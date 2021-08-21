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
ms.openlocfilehash: 22075c68ef30fda7360f25e76c84dbffbf7e306335a0ef20bda45559cb6dac09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472286"
---
# <a name="ivmguestossuitemask-property"></a>Propriedade IVMGuestOS:: SuiteMask

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>"0x00000400"</dt> </dl> | Windows O Server 2003, Web Edition está instalado.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, o Compute Cluster Edition está instalado.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows o server 2008 R2 datacenter, o Windows server 2008 datacenter, o Windows server 2003, o datacenter Edition ou o Windows 2000 datacenter server está instalado.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | Windows server 2008 R2 Enterprise, Windows server 2008 Enterprise, Windows server 2003, Edição Enterprise ou Windows 2000 Advanced server está instalado.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Windows O XP Embedded está instalado.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows o vista home Premium, Windows vista home Basic ou Windows XP home Edition está instalado.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Há suporte para Área de Trabalho Remota, mas há suporte para apenas uma sessão interativa.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | O Microsoft Small Business Server já foi instalado no sistema, mas pode ter sido atualizado para outra versão do Windows.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | O Microsoft Small Business Server é instalado com a licença de cliente restritiva em vigor.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | Windows Armazenamento server 2003 R2 ou Windows Armazenamento server 2003 está instalado.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | O Serviços de Área de Trabalho Remota está instalado. Esse valor é sempre definido.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows O servidor primário está instalado.<br/>                                                                                                                           |



 

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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

