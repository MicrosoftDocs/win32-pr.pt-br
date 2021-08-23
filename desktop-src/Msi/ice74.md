---
description: ICE74 verifica se a propriedade FASTOEM não foi autor na tabela Property.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3120b0f4cd40acc53a1bcd3623dac33941a7f5da39bc538781e4ffd1d56345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328316"
---
# <a name="ice74"></a>ICE74

ICE74 verifica se a [**propriedade FASTOEM**](fastoem.md) não foi autor na [tabela Property](property-table.md).

A [**propriedade FASTOEM**](fastoem.md) permite que os OEMs reduzam o tempo necessário para instalar Windows instalador pela primeira vez. Ele não pode ser usado após a primeira instalação. A **propriedade FASTOEM** não deve ser autor na tabela Propriedade porque isso interfere nas instalações subsequentes para manutenção, remoção ou reparo do aplicativo.

ICE74 também verifica se a propriedade [**UpgradeCode**](upgradecode.md) [](property-table.md)foi autor na tabela Property e se seu valor não é um GUID nulo, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Resultado

O ICE74 pode postar os seguintes erros.



| Erro ICE74                                                                       | Descrição                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| A [**propriedade FASTOEM**](fastoem.md) não pode ser autor na tabela Property. | A [**propriedade FASTOEM**](fastoem.md) foi definida na tabela Property.                             |
| ' \[ 2 \] ' não é um [**UpgradeCode válido.**](upgradecode.md)                        | Um GUID nulo foi inserido para a [**propriedade UpgradeCode**](upgradecode.md) na tabela Property. |



 

O ICE74 pode postar o aviso a seguir.



| Aviso ICE74                                                                                                                                                                                             | Descrição                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| A [**propriedade UpgradeCode**](upgradecode.md) não é autor na tabela Property. É altamente recomendável que os autores de pacotes de instalação especifiquem **um UpgradeCode** para seu aplicativo. | A [**propriedade UpgradeCode**](upgradecode.md) não é autor na tabela Property. |



 

## <a name="example"></a>Exemplo

ICE74 relata o seguinte erro se a [**propriedade FASTOEM**](fastoem.md) estiver definida: o FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade                   | Valor |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Para corrigir esse erro, remova a [**propriedade FASTOEM**](fastoem.md) da Tabela de Propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedade FASTOEM**](fastoem.md)
</dt> <dt>

[Tabela de propriedades](property-table.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



