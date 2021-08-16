---
description: Assemblies lado a lado são usados com os seguintes tipos de arquivos de manifesto e configuração. Manifestos e configurações são arquivos XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referência de arquivos de manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87636a8a4e5398cf9bb274d5ea8b9e7620104989322a20138a162ca45d9caf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142059"
---
# <a name="manifest-files-reference"></a>Referência de arquivos de manifesto

Assemblies lado a lado são usados com os seguintes tipos de arquivos de manifesto e configuração. Manifestos e configurações são arquivos XML.



| Manifest                                                               | Descrição                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifestos do assembly](assembly-manifests.md)                           | Descreve os nomes, versões, recursos e dependências de assembly de assemblies lado a lado.                                                                                                               |
| [Manifestos do aplicativo](application-manifests.md)                     | Descreve os nomes e as versões de assemblies compartilhados lado a lado aos que o aplicativo deve se vincular em tempo de executar e também pode conter metadados para assemblies particulares lado a lado usados pelo aplicativo. |
| [Arquivos de configuração de aplicativo](application-configuration-files.md) | Redireciona as versões de assembly de dependências de assembly usando [a configuração por aplicativo.](per-application-configuration.md)                                                                            |
| [Publisher Arquivos de configuração](publisher-configuration-files.md)     | Redireciona as versões de assembly de dependências de assembly por assembly usando uma [configuração de publicador](publisher-configuration.md).                                                              |



 

Para uma listagem do esquema do arquivo de manifesto, consulte [Esquema de arquivo de manifesto](manifest-file-schema.md).

Para ver uma lista do esquema do arquivo de configuração de aplicativo, consulte Esquema do arquivo de [configuração de aplicativo.](application-configuration-file-schema.md)

Para ver uma lista do esquema do arquivo de configuração do publicador, consulte Publisher esquema de [arquivo de configuração](publisher-configuration-file-schema.md).

Outras tecnologias estendem o formato usado pelo Windows de versão e manifestos de configuração. Os desenvolvedores devem consultar a documentação específica da tecnologia que está sendo usada para obter informações sobre o formato do manifesto. Por exemplo:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [UAC (Controle de Conta de Usuário)](/previous-versions/bb756929(v=msdn.10))

 

 
