---
title: Propriedade IVMGuestOS SuiteMask (VPCCOMInterfaces. h)
description: Recupera o SuiteMask do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Propriedade SuiteMask Virtual PC
- Propriedade SuiteMask Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645172"
---
# <a name="ivmguestossuitemask-property"></a>Propriedade IVMGuestOS:: SuiteMask

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o SuiteMask do sistema operacional convidado em execução na máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Valor da propriedade

A máscara do pacote. Há suporte para os valores de cadeia de caracteres a seguir.



| Valor                                                                                   | Significado                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000004</dt> </dl> | Os componentes do Microsoft BackOffice são instalados.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | O Windows Server 2003, Web Edition está instalado.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | O Windows Server 2003, Compute Cluster Edition, está instalado.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | O Windows Server 2008 R2 Datacenter, o Windows Server 2008 Datacenter, o Windows Server 2003, o Datacenter Edition ou o Windows 2000 Datacenter Server está instalado.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | O Windows Server 2008 R2 Enterprise, o Windows Server 2008 Enterprise, o Windows Server 2003, Enterprise Edition ou o Windows 2000 Advanced Server está instalado.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | O Windows XP Embedded está instalado.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | O Windows Vista Home Premium, o Windows Vista Home Basic ou o Windows XP Home Edition está instalado.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | O Windows Storage Server 2003 R2 ou o Windows Storage Server 2003 está instalado.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | O Serviços de Área de Trabalho Remota está instalado. Esse valor é sempre definido.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | O Windows Home Server está instalado.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro é **NULL**.<br/>                           |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>               | A VM não está em execução.<br/>                               |
| <dl> <dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt> </dl> | Os componentes de integração não estão instalados nesta VM.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

