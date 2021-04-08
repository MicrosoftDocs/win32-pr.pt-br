---
description: Usando assemblies lado a lado como um recurso
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: Usando assemblies lado a lado como um recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b97265b48f4ce8f3c87a87ec4ca9ea2b8252819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920825"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a>Usando assemblies lado a lado como um recurso

Você pode adicionar um manifesto a um aplicativo como um recurso no arquivo de cabeçalho executável binário do aplicativo. O valor da ID de \_ recurso de manifesto \_ determina como as dependências de assembly lado a lado descritas no manifesto são usadas pelo carregador.

Se você definir a ID de recurso de manifesto \_ \_ como 1, o carregador usará as dependências de assembly lado a lado especificadas no manifesto como o padrão de processo. Todos os plug-ins também usam esse padrão de processo.

A tabela a seguir resume como o carregador usa o manifesto para valores diferentes da ID de recurso de manifesto \_ \_ quando o aplicativo é compilado com o \_ sinalizador habilitado para reconhecimento de DISOLATION \_ . Observe que os valores 1-16 são reservados para uso pelo Windows XP. Um desenvolvedor poderá usar outros valores se quiser gerenciar os contextos de ativação usando as funções descrevem na referência do [contexto de ativação](activation-context-reference.md).



| Valor da \_ ID do recurso de manifesto \_ | O manifesto especifica o padrão do processo? | Usar para importações estáticas? | Usar para um EXE? | Usar para uma DLL? | Usa a versão lado a lado de assemblies, se compilado com-DISOLATION com \_ reconhecimento \_ habilitado? |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| 1                               | Sim                                     | Sim                     | Sim             | Não             | Sim                                                                                   |
| 2                               | Não                                      | Sim                     | Sim             | Sim            | Sim                                                                                   |
| 3                               | Não                                      | Não                      | Sim             | Sim            | Sim                                                                                   |



 

\_ \_ A ID de recurso de manifesto 1 deve ser usada para aplicativos que não hospedam plug-ins. Use \_ \_ a ID de recurso de manifesto 1 quando todas as partes do aplicativo devem usar a versão do assembly lado a lado especificado no manifesto. Para obter mais informações, consulte [habilitando um assembly em um aplicativo sem extensões](enabling-an-assembly-in-an-application-without-extensions.md).

A \_ \_ ID de recurso de manifesto 2 deve ser usada para aplicativos que hospedam controles ou plug-ins de terceiros. Nesse caso, o manifesto afeta todos os assemblies lado a lado que estão sendo carregados pelo carregamento estático, chamadas para DllMain e chamadas redirecionadas por-DISOLATION com \_ reconhecimento \_ habilitado. Para obter mais informações, consulte [habilitando um assembly em um aplicativo que hospeda uma dll, extensão ou painel de controle](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

\_ \_ A ID de recurso de manifesto 3 deve ser usada para redirecionar chamadas \_ somente com reconhecimento de DISOLATION \_ habilitado. O carregamento por outros métodos não é afetado.

 

 



