---
description: ICE14 valida a tabela de recursos de um banco de dados Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296914"
---
# <a name="ice14"></a>ICE14

O ICE14 valida o seguinte para os recursos:

-   Os recursos pai raiz não têm o conjunto de bits msidbFeatureAttributesFollowParent na coluna atributos da tabela de [recursos](feature-table.md). Um recurso raiz não tem um pai.
-   Que nenhum recurso tenha a mesma entrada nas \_ colunas pai de recurso e recurso da [tabela de recursos](feature-table.md). Nenhum recurso pode ser seu próprio pai.

## <a name="result"></a>Resultado

ICE14 posta uma mensagem de erro se encontrar um recurso raiz com o conjunto de bits msidbFeatureAttributesFollowParent ou um recurso com entradas idênticas nas \_ colunas pai do recurso e do recurso da tabela de recursos.

## <a name="example"></a>Exemplo

ICE14 retornaria os seguintes erros para o exemplo a seguir:

-   O esporte do recurso tem o mesmo valor nas colunas pai do recurso e \_ do recurso da tabela de arquivos.
-   O esporte do recurso raiz tem o conjunto de bits msidbFeatureAttributesFollowParent.

Na árvore de recursos deste exemplo, esporte é o recurso raiz e um pai dos recursos de nada e de futebol. Freestyle é um recurso filho de nada. TouchFootball é um recurso filho de futebol.

[Tabela de recursos](feature-table.md) (parcial)



| Recurso       | Atributos | Pai do recurso \_ |
|---------------|------------|-----------------|
| Esporte         | 4          | Esporte           |
| Swimming      | 1          | Esporte           |
| Comemorar      | 4          | Esporte           |
| Freestyle     | 1          | Swimming        |
| TouchFootball | 4          | Comemorar        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



