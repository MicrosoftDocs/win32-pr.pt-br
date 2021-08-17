---
description: Especifica o número máximo de imagens de um cabeçalho de grupo de imagens (GOP) para o próximo cabeçalho GOP.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propriedade AVEncMPVGOPSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7c82ae5c613bb3e78069be3f39f652d840e19c5d62d095fe020f4186bf975f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119258446"
---
# <a name="avencmpvgopsize-property"></a>Propriedade AVEncMPVGOPSize

Especifica o número máximo de imagens de um cabeçalho de grupo de imagens (GOP) para o próximo cabeçalho GOP.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPVGOPSize**

## <a name="property-value"></a>Valor da propriedade

Os codificadores podem implementar essa propriedade como um conjunto enumerado ou como um intervalo linear.

## <a name="remarks"></a>Comentários

Defina essa propriedade antes de iniciar uma gravação.

**Aplica-se a Windows 8:** O tamanho de GOP codificado deve ser menor ou igual ao número especificado por meio dessa propriedade, a fim de manter o mesmo padrão de quadro B definido por [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) em toda a GOP ou devido à alteração de cena. Por exemplo, quando o número de quadros B em um GOP é especificado como 2 e o tamanho de GOP é 11, o codificador deve produzir o tamanho de GOP de 10 quadros ou menos. Quando a alteração de cena ocorre no meio de um GOP, o codificador também pode inserir o quadro-chave e produzir GOP menores.

O tamanho 0 do GOP é dependente do codificador e os codificadores podem escolher diferentes tamanhos de GOP com base em sua implementação/qualidade/desempenho. Os codificadores devem respeitar o tamanho do GOP e truncar os quadros B nesse caso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




