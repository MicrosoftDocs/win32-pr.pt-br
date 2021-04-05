---
title: Propriedade IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces. h)
description: Indica se este objeto tem controle exclusivo sobre o dispositivo de teclado da VM.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Propriedade HasExclusiveAccess Virtual PC
- Propriedade HasExclusiveAccess Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, Propriedade HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086222"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>Propriedade IVMKeyboard:: HasExclusiveAccess

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica se este objeto tem controle exclusivo sobre o dispositivo de teclado da máquina virtual (VM).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>Valor da propriedade

**True** se o acesso exclusivo ao dispositivo de teclado da VM tiver sido adquirido; caso contrário, **false** .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                   | Significado                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                        | O parâmetro *isexclusive* é **nulo**.<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                   | O modo exclusivo solicitado já está definido para este dispositivo. Isso pode ocorrer ao tentar definir o modo exclusivo quando ele já foi adquirido ou ao tentar liberar o modo exclusivo quando ele não foi adquirido anteriormente.<br/> |
| <dl> <dt>VM \_ E & \_ set \_ Exclusive \_ mode \_ falham</dt> <dt>0xA0040825</dt> </dl> | Falha ao definir ou liberar o modo exclusivo conforme solicitado. Isso pode ocorrer porque a VM não está mais em execução ou porque outro processo já adquiriu o modo exclusivo no dispositivo de teclado da VM.<br/>                                 |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                     | A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

