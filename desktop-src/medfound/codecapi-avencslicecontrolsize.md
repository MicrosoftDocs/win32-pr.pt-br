---
description: Especifica o tamanho da fatia em unidades de megabytes (MB), bits ou MB de linha.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Propriedade CODECAPI_AVEncSliceControlSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d068d8b2c5fc15fdb82c3ffe068e6926d28228a19367114067e02ebc44b03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035344"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>\_Propriedade CODECAPI AVEncSliceControlSize

Especifica o tamanho da fatia em unidades de megabytes (MB), bits ou MB de linha.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>Comentários

**Codificadores H. 264/AVC:**

O significado do valor de CODECAPI \_ AVEncSliceControlSize é controlado pela propriedade [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) . A tabela a seguir ilustra como as \_ Propriedades CODECAPI AVEncSliceControlSize e CODECAPI \_ AVEncSliceControlMode controlam o tamanho e o número de fatias em um quadro.



| Configuração de CODECAPI \_ AVEncSliceControlMode | Significado do valor                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Este é um inteiro que indica o tamanho de cada fatia no quadro em unidades de macroblocos. <br/> O codificador deve rejeitar a configuração quando o valor for maior que o número de macroblocos no quadro.<br/>                                                                                                                                                                         |
| 1                                       | Este é um inteiro que indica o tamanho de cada fatia no quadro em unidades de bits. <br/> O codificador deve iniciar uma nova fatia no macrobloco que faz com que o número de bits na fatia exceda esse valor (portanto, o tamanho de cada fatia sempre será menor ou igual a esse valor). Isso significa que o tamanho da última fatia pode ser significativamente menor do que esse valor. <br/> |
| 2                                       | Esse é um inteiro que indica o tamanho de cada fatia no quadro em unidades de macrobloco linhas. <br/> O codificador deve rejeitar a configuração quando o valor for maior que o número de linhas macrobloco no quadro.<br/>                                                                                                                                                                 |



 

Se o aplicativo não definir um valor para [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), o codificador deverá retornar um erro.

O padrão recomendado é ter uma única fatia para o quadro inteiro.

Alguns codificadores podem codificar fatias em paralelo e, portanto, o desempenho pode ser afetado dependendo das configurações de controle de fatia. Por exemplo, codificar um quadro como uma única fatia pode ser mais lento do que se o quadro fosse codificado como várias fatias.

As configurações de controle de fatia são dinâmicas e podem ser alteradas durante a sessão de codificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




