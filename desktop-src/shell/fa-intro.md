---
description: 'Esta seção sobre tipos de arquivo e associações de arquivo é organizada da seguinte maneira:'
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: Tipos de arquivo e associações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf84bbf44475d32768d2359d3723952ada843c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169447"
---
# <a name="file-types-and-file-associations"></a>Tipos de arquivo e associações de arquivo

Esta seção sobre tipos de arquivo e associações de arquivo é organizada da seguinte maneira:

-   [registro de Aplicativo](app-registration.md)
-   [Tipos de arquivo](fa-file-types.md)
-   [Como escolher uma extensão de tipo de arquivo](how-to-choose-a-file-type-extension.md)
-   [Como definir atributos de tipo de arquivo](how-to-define-file-type-attributes.md)
-   [Como incluir um aplicativo na caixa de diálogo abrir com](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Como excluir um aplicativo da caixa de diálogo abrir com para tipos de arquivo não associados](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [Como funcionam as associações de arquivo](fa-how-work.md)
-   [Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
-   [Como registrar Propriedades personalizadas e layout para o tipo de arquivo](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [Verificador de tipo de arquivo](file-type-verifier.md)
-   [Como usar o verificador de tipo de arquivo](how-to-use-the-file-type-verifier.md)
-   [Manipuladores de tipo de arquivo](fa-file-extensions.md)
-   [Identificadores programáticos](fa-progids.md)
-   [Como registrar um tipo de arquivo para um novo aplicativo](how-to-register-a-file-type-for-a-new-application.md)
-   [Tipos observados](fa-perceivedtypes.md)
-   [Matrizes de associação](fa-associationarray.md)

## <a name="additional-resources"></a>Recursos adicionais

-   Definir o acesso do programa e padrões do computador (SPAD) é um painel de controle do Windows que permite aos usuários com privilégio administrativo definir um padrão de máquina e ocultar ou mostrar um aplicativo. Aplicativos de mídia, email, navegador, Messenger e Java são exemplos de aplicativos registrados em SPAD. Defina os programas padrão (SYDP) como um painel de controle do Windows, que funciona com privilégios limitados e permite que os usuários definam um padrão de usuário. Qualquer aplicativo pode ser registrado no SYDP. Para obter informações sobre o registro de aplicativo SPAD e SYDP, consulte [diretrizes para associações de arquivo e programas padrão](appguide-fa-defpro.md)e [definir o acesso do programa e padrões do computador (SPAD)](cpl-setprogramaccess.md).
-   Para obter informações conceituais relacionadas, consulte [visão geral de verbos e associações de arquivo](fa-verbs.md).
-   Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](nse-implement.md).

Para obter a documentação de referência relacionada, consulte os seguintes tópicos:

-   Para executar um verbo em um item de Shell, consulte o método [**InvokeVerb**](folderitem-invokeverb.md) .
-   Para recuperar uma coleção de verbos que podem ser executados em um item de Shell, consulte o método [**Verbs**](folderitem-verbs.md) .
-   Para executar uma operação em um arquivo especificado, consulte as funções [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .
-   Para obter uma lista de tipos observados padrão, consulte a enumeração [**percebida**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Para recuperar o tipo percebido de um arquivo com base em sua extensão, consulte a função [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

 

 



