---
description: ICE74 verifica se a propriedade FASTOEM não foi criada na tabela de propriedades.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749588"
---
# <a name="ice74"></a>ICE74

ICE74 verifica se a propriedade [**FASTOEM**](fastoem.md) não foi criada na [tabela de propriedades](property-table.md).

A propriedade [**FASTOEM**](fastoem.md) permite que os OEMs reduzam o tempo necessário para instalar Windows Installer aplicativos pela primeira vez. Ele não pode ser usado após a primeira instalação. A propriedade **FASTOEM** não deve ser criada na tabela de propriedades porque ela interfere nas instalações subsequentes para a manutenção, remoção ou reparo do aplicativo.

ICE74 também verifica se a propriedade [**UpgradeCode**](upgradecode.md) é criada na [tabela de propriedades](property-table.md)e se seu valor não é um GUID nulo, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Resultado

ICE74 pode postar os erros a seguir.



| Erro de ICE74                                                                       | Descrição                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| A propriedade [**FASTOEM**](fastoem.md) não pode ser criada na tabela de propriedades. | A propriedade [**FASTOEM**](fastoem.md) foi definida na tabela de propriedades.                             |
| ' \[ 2 \] ' não é um [**UpgradeCode**](upgradecode.md)válido.                        | Um GUID nulo foi inserido para a propriedade [**UpgradeCode**](upgradecode.md) na tabela de propriedades. |



 

ICE74 pode postar o aviso a seguir.



| Aviso de ICE74                                                                                                                                                                                             | Descrição                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| A propriedade [**UpgradeCode**](upgradecode.md) não foi criada na tabela de propriedades. É altamente recomendável que os autores de pacotes de instalação especifiquem um **UpgradeCode** para seu aplicativo. | A propriedade [**UpgradeCode**](upgradecode.md) não foi criada na tabela de propriedades. |



 

## <a name="example"></a>Exemplo

ICE74 relata o seguinte erro se a propriedade [**FASTOEM**](fastoem.md) estiver definida: o FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade                   | Valor |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Para corrigir esse erro, remova a propriedade [**FASTOEM**](fastoem.md) da tabela de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedade FASTOEM**](fastoem.md)
</dt> <dt>

[Tabela de propriedades](property-table.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



