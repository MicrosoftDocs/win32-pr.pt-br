---
title: Interface IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera informações sobre o computador host. Um objeto IVMHostInfo é retornado da propriedade IVMVirtualPC HostInfo.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- Virtual PC de interface IVMHostInfo
- Virtual PC de interface IVMHostInfo, descrito
topic_type:
- apiref
api_name:
- IVMHostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da45459379c468839b0bf48ae134db1885ea25acce5ac3befa289ae15ee6fe8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974256"
---
# <a name="ivmhostinfo-interface"></a>Interface IVMHostInfo

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera informações sobre o computador host. Um objeto **IVMHostInfo** é retornado da propriedade [**IVMVirtualPC:: HostInfo**](ivmvirtualpc-hostinfo.md) .

## <a name="members"></a>Membros

A interface **IVMHostInfo** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHostInfo** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMHostInfo** tem essas propriedades.



| Propriedade                                                                                  | Tipo de acesso          | Descrição                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Somente leitura<br/> | As letras da unidade associadas aos dispositivos de CD e DVD do host.<br/>                              |
| [**FloppyDrives**](ivmhostinfo-floppydrives.md)<br/>                               | Somente leitura<br/> | As letras da unidade associadas às unidades de disquete do host.<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Somente leitura<br/> | O número de processadores lógicos no computador host.<br/>                                   |
| [**Memória**](ivmhostinfo-memory.md)<br/>                                           | Somente leitura<br/> | A quantidade total de memória física no computador host, em megabytes.<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | Somente leitura<br/> | A quantidade de memória física disponível no computador host, em megabytes.<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | Somente leitura<br/> | A quantidade de memória física disponível no computador host, em megabytes, como uma cadeia de caracteres.<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | Somente leitura<br/> | A quantidade total de memória física no computador host, em megabytes, como uma cadeia de caracteres.<br/>     |
| [**TECNOLOGIA**](ivmhostinfo-mmx.md)<br/>                                                 | Somente leitura<br/> | Indica se o processador dá suporte ao conjunto de instruções MMX.<br/>                       |
| [**Adaptadores**](ivmhostinfo-networkadapters.md)<br/>                         | Somente leitura<br/> | Uma coleção enumerável de NICs no computador host.<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | Somente leitura<br/> | Uma coleção enumerável de endereços TCP/IP no computador host.<br/>                       |
| [**Operacional**](ivmhostinfo-operatingsystem.md)<br/>                         | Somente leitura<br/> | O sistema operacional em execução no computador host.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Somente leitura<br/> | A versão principal do sistema operacional em execução no computador host.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Somente leitura<br/> | A versão secundária do sistema operacional em execução no computador host.<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | Somente leitura<br/> | As informações de service pack do sistema operacional em execução no computador host.<br/>       |
| [**OSVersionstring**](ivmhostinfo-osversionstring.md)<br/>                         | Somente leitura<br/> | A versão do sistema operacional em execução no computador host.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Somente leitura<br/> | A porta paralela do host que pode ser anexada ao convidado.<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Somente leitura<br/> | O número de processadores físicos no computador host.<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Somente leitura<br/> | A lista de recursos com suporte pelo processador do host.<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | Somente leitura<br/> | O fabricante do processador do host.<br/>                                                 |
| [**ProcessorSpeed**](ivmhostinfo-processorspeed.md)<br/>                           | Somente leitura<br/> | A velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz).<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | Somente leitura<br/> | A velocidade do processador do host, em megahertz ou gigahertz, como uma cadeia de caracteres.<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | Somente leitura<br/> | A versão do processador do host.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Somente leitura<br/> | Os nomes de porta serial associados às portas seriais do host.<br/>                                |
| [**SSE**](ivmhostinfo-sse.md)<br/>                                                 | Somente leitura<br/> | Indica se o processador dá suporte ao conjunto de instruções SSE.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Somente leitura<br/> | Indica se o processador dá suporte ao conjunto de instruções SSE2.<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | Somente leitura<br/> | Indica se o processador dá suporte ao conjunto de instruções 3DNow.<br/>                     |
| [**UTCTime**](ivmhostinfo-utctime.md)<br/>                                         | Somente leitura<br/> | A hora UTC no computador host.<br/>                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



 

