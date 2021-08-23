---
title: Propriedade IVMGuestOS TerminalServicesInitialized (VPCCOMInterfaces. h)
description: Status de Serviços de Área de Trabalho Remota no sistema operacional convidado.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- Propriedade TerminalServicesInitialized Virtual PC
- Propriedade TerminalServicesInitialized Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595ae6028bea1984a320a699d204e4d3c23c1ca44e021cbbd994bbc5b832655a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512146"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a>Propriedade IVMGuestOS:: TerminalServicesInitialized

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o status de Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) no sistema operacional convidado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a>Valor da propriedade

O status de inicialização.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida e Serviços de Área de Trabalho Remota foi inicializada. O valor da propriedade retornada indica se Serviços de Área de Trabalho Remota está disponível no sistema operacional convidado.<br/> |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                       | O recurso componentes de integração está em execução, mas Serviços de Área de Trabalho Remota ainda não foi inicializado.<br/>                                                                                               |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro é **NULL**.<br/>                                                                                                                                                                       |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual (VM) deve estar em execução para esta operação.<br/>                                                                                                                                     |
| <dl> <dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt> </dl> | O recurso componentes de integração não está em execução no sistema operacional convidado.<br/>                                                                                                                 |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                                                                                                |



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

 

