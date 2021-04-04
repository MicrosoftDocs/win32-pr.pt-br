---
title: Propriedade thumbnail IVMDisplay (VPCCOMInterfaces. h)
description: Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual. | Propriedade thumbnail IVMDisplay (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propriedade de miniatura Virtual PC
- Propriedade thumbnail Virtual PC, interface IVMDisplay
- Virtual PC de interface IVMDisplay, propriedade Thumbnail
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
ms.openlocfilehash: 0466af2552fbb108f31de94b3f970d6e7d5571b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930277"
---
# <a name="ivmdisplaythumbnail-property"></a>Propriedade IVMDisplay:: thumbnail

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variante do tipo VT \_ variante de matriz \| VT \_ que contém entradas do tipo VT \_ UI4, uma para cada pixel na miniatura.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="remarks"></a>Comentários

Essa interface retorna a miniatura com menos eficiência do que o método [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , mas é utilizável de clientes de script. A miniatura tem sempre 64 pixels de largura por 48 pixels de altura. Cada pixel é de 32 bits. Os primeiros 64 elementos na matriz são a primeira linha de pixels na miniatura, os próximos 64 elementos são a segunda linha e assim por diante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

