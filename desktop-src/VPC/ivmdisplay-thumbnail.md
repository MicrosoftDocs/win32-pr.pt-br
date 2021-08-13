---
title: Propriedade De miniatura IVMDisplay (VPCCOMInterfaces.h)
description: Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual. | Propriedade De miniatura IVMDisplay (VPCCOMInterfaces.h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propriedade thumbnail Pc Virtual
- Propriedade thumbnail Pc Virtual, interface IVMDisplay
- COMPUTADOR Virtual da interface IVMDisplay, propriedade Thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a558a551972bb76558dcd60223d8ddc29783aeaa23e6dbe9263f34642c1c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473326"
---
# <a name="ivmdisplaythumbnail-property"></a>Propriedade IVMDisplay::Thumbnail

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variante do tipo VT ARRAY VT VARIANT que contém entradas do tipo \_ \| \_ VT UI4, uma para \_ cada pixel na miniatura.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="remarks"></a>Comentários

Essa interface retorna a miniatura com menos eficiência do que [**\_ o método GenerateThumbnail,**](ivmdisplay--generatethumbnail.md) mas pode ser usado de clientes de script. A miniatura sempre tem 64 pixels de largura por 48 pixels de altura. Cada pixel tem 32 bits. Os primeiros 64 elementos na matriz são a primeira linha de pixels na miniatura, os próximos 64 elementos são a segunda linha e assim por diante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay é definido como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

