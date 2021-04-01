---
description: Os assemblies lado a lado são usados com os seguintes tipos de arquivos de manifesto e de configuração. Manifestos e configurações são arquivos XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referência de arquivos de manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090206"
---
# <a name="manifest-files-reference"></a>Referência de arquivos de manifesto

Os assemblies lado a lado são usados com os seguintes tipos de arquivos de manifesto e de configuração. Manifestos e configurações são arquivos XML.



| Manifest                                                               | Descrição                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manifestos de assembly](assembly-manifests.md)                           | Descreve os nomes, as versões, os recursos e as dependências de assembly de assemblies lado a lado.                                                                                                               |
| [Manifestos do aplicativo](application-manifests.md)                     | Descreve os nomes e as versões de assemblies compartilhados lado a lado que o aplicativo deve associar em tempo de execução e também pode conter metadados para assemblies particulares lado a lado usados pelo aplicativo. |
| [Arquivos de configuração de aplicativo](application-configuration-files.md) | Redireciona as versões de assembly das dependências de assembly usando [a configuração por aplicativo](per-application-configuration.md).                                                                            |
| [Arquivos de configuração do Publicador](publisher-configuration-files.md)     | Redireciona as versões de assembly de dependências de assembly em uma base por assembly usando uma [configuração de Publicador](publisher-configuration.md).                                                              |



 

Para obter uma lista do esquema do arquivo de manifesto, consulte [manifesto do arquivo de manifest](manifest-file-schema.md).

Para obter uma lista do esquema de arquivo de configuração de aplicativo, consulte [esquema de arquivo de configuração de aplicativo](application-configuration-file-schema.md).

Para obter uma lista do esquema do arquivo de configuração do Publicador, consulte [esquema do arquivo de configuração do Publicador](publisher-configuration-file-schema.md).

Outras tecnologias estendem o formato usado pelos manifestos de configuração e controle de versão do Windows. Os desenvolvedores devem consultar a documentação específica da tecnologia que está sendo usada para obter informações sobre o formato do manifesto. Por exemplo:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Common Language Runtime](/dotnet/standard/clr)
-   [UAC (Controle de Conta de Usuário)](/previous-versions/bb756929(v=msdn.10))

 

 
