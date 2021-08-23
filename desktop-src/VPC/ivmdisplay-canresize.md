---
title: Propriedade IVMDisplay CanResize (VPCCOMInterfaces.h)
description: Determina se o Convidado permite alterações de resolução.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Propriedade CanResize Pc Virtual
- Propriedade CanResize Pc Virtual, interface IVMDisplay
- INTERFACE IVMDisplay Pc Virtual , propriedade CanResize
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b55bc4ab9599b119988b68df022c098048aeee9ea19194e2c3dcbfdaefde479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473576"
---
# <a name="ivmdisplaycanresize-property"></a>Propriedade IVMDisplay::CanResize

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se o Convidado permite alterações de resolução.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a>Valor da propriedade

**VARIANT \_ TRUE** se o Convidado permitir alterações de resolução e **VARIANT FALSE \_ caso** contrário.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                                                                              |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                            | O parâmetro é **NULL.**<br/>                                                                                                                 |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                    | A configuração é desconhecida.<br/>                                                                                                              |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual deve estar em execução para essa operação.<br/>                                                                                    |
| <dl> <dt>VM \_ E \_ NO \_ DISPLAY</dt> <dt>0XA0040850</dt> </dl>                    | Não foi encontrado nenhum dispositivo de vídeo para a máquina virtual.<br/>                                                                                   |
| <dl> <dt>VM \_ O \_ RECURSO DE \_ ADIÇÕES E NÃO \_ \_ ESTÁ</dt> <dt>0XA0040505</dt> </dl> | O recurso de componentes de integração não está disponível; os componentes de integração não estão instalados ou o recurso foi desabilitado.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay é definido como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

