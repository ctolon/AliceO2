# Copyright 2019-2020 CERN and copyright holders of ALICE O2.
# See https://alice-o2.web.cern.ch/copyright for details of the copyright holders.
# All rights not expressly granted are reserved.
#
# This software is distributed under the terms of the GNU General Public
# License v3 (GPL Version 3), copied verbatim in the file "COPYING".
#
# In applying this license CERN does not waive the privileges and immunities
# granted to it by virtue of its status as an Intergovernmental Organization
# or submit itself to any jurisdiction.

o2_add_library(DataFormatsTOF
               SOURCES src/Cluster.cxx
                       src/CalibInfoTOFshort.cxx
                       src/CalibInfoTOF.cxx
                       src/CalibLHCphaseTOF.cxx
                       src/CalibTimeSlewingParamTOF.cxx
                       src/CTF.cxx
                       src/CalibInfoCluster.cxx
                       src/CosmicInfo.cxx
                       src/Diagnostic.cxx
                       src/TOFFEElightInfo.cxx
               PUBLIC_LINK_LIBRARIES O2::ReconstructionDataFormats
                                     O2::GPUCommon
                                     Boost::serialization)

o2_target_root_dictionary(DataFormatsTOF
                          HEADERS include/DataFormatsTOF/Cluster.h
                                  include/DataFormatsTOF/CalibInfoTOFshort.h
                                  include/DataFormatsTOF/CalibInfoTOF.h
                                  include/DataFormatsTOF/CalibLHCphaseTOF.h
                                  include/DataFormatsTOF/CalibTimeSlewingParamTOF.h
                                  include/DataFormatsTOF/RawDataFormat.h
                                  include/DataFormatsTOF/CompressedDataFormat.h
                                  include/DataFormatsTOF/CTF.h
                                  include/DataFormatsTOF/CalibInfoCluster.h
                                  include/DataFormatsTOF/CosmicInfo.h
                                  include/DataFormatsTOF/TOFFEElightInfo.h
                                  include/DataFormatsTOF/Diagnostic.h)
