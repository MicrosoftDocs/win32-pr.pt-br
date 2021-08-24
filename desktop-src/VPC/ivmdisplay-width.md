---
title: Propriedade IvMDisplay Width (VPCCOMInterfaces.h)
description: Largura da exibição da VM, em pixels.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Propriedade Width Pc Virtual
- Propriedade Width Pc Virtual , interface IVMDisplay
- INTERFACE IVMDisplay Pc Virtual , propriedade Width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db106804f81f52b669b90920699761061d97fb3412dd58b761f7da1701ec53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654216"
---
# <a name="ivmdisplaywidth-property"></a>Propriedade IVMDisplay::Width

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a largura da exibição da máquina virtual (VMs) em pixels.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a>Valor da propriedade

A largura, em pixels.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                                 |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>              | O parâmetro é **NULL.**<br/>                                    |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0xA0040206</dt> </dl> | A máquina virtual deve estar em execução para essa operação.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | A máquina virtual não é válida ou não está em execução no momento.<br/> |
| <dl> <dt>VM \_ E \_ NO \_ DISPLAY</dt> <dt>0XA0040850</dt> </dl>      | Não é possível localizar uma exibição válida para a máquina virtual.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ocorreu um erro inesperado.<br/>                             |



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

 

