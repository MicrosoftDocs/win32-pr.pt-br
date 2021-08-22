---
title: Propriedade IvMKeyboard HasExclusiveAccess (VPCCOMInterfaces.h)
description: Indica se esse objeto tem controle exclusivo sobre o dispositivo de teclado da VM.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Propriedade HasExclusiveAccess Pc Virtual
- Propriedade HasExclusiveAccess Pc Virtual, interface IVMKeyboard
- INTERFACE IVMKeyboard Pc Virtual , propriedade HasExclusiveAccess
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
ms.openlocfilehash: c01e13e331824a0d1b6834cbb27da7eb4b5420a3cd3dbec94cdbdd494c79c95b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136719"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>Propriedade IVMKeyboard::HasExclusiveAccess

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica se esse objeto tem controle exclusivo sobre o dispositivo de teclado da máquina virtual (VM).

Essa propriedade é leitura/gravação.

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

**TRUE** se o acesso exclusivo ao dispositivo de teclado da VM tiver sido adquirido; caso contrário, **FALSE.**

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                   | Significado                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                        | O *parâmetro isExclusive* é **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                   | O modo exclusivo solicitado já está definido para esse dispositivo. Isso pode acontecer ao tentar definir o modo exclusivo quando ele já tiver sido adquirido ou ao tentar liberar o modo exclusivo quando ele não tiver sido adquirido anteriormente.<br/> |
| <dl> <dt>VM \_ E \_ SET EXCLUSIVE MODE \_ \_ \_ FAIL</dt> <dt>0XA0040825</dt> </dl> | Falha ao definir ou liberar o modo exclusivo conforme solicitado. Isso pode ser porque a VM não está mais em execução ou porque outro processo já adquiriu o modo exclusivo no dispositivo de teclado da VM.<br/>                                 |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                     | A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

