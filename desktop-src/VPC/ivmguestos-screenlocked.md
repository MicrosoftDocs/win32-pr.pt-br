---
title: Propriedade IVMGuestOS ScreenLocked (VPCCOMInterfaces. h)
description: Indica se a tela no sistema operacional convidado está bloqueada.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Propriedade ScreenLocked Virtual PC
- Propriedade ScreenLocked Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade ScreenLocked
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009468"
---
# <a name="ivmguestosscreenlocked-property"></a>Propriedade IVMGuestOS:: ScreenLocked

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica se a tela no sistema operacional convidado está bloqueada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a>Valor da propriedade

**Variante \_ TRUE** se a tela estiver bloqueada no sistema operacional convidado; caso contrário, **Variant \_ false** .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                    |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro é **NULL**.<br/>                                                       |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual (VM) deve estar em execução para esta operação.<br/>                     |
| <dl> <dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt> </dl> | O recurso componentes de integração não está habilitado no sistema operacional convidado.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

