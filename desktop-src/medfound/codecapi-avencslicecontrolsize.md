---
description: Especifica o tamanho da fatia em unidades de megabytes (MB), bits ou MB de linha.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Propriedade CODECAPI_AVEncSliceControlSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089785"
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
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




