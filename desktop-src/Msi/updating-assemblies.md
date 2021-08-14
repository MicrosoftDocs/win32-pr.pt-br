---
description: As informações neste tópico identificam as diretrizes recomendadas para atualizar assemblies usando patches Windows Instalador.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Atualizando assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65467613206f3736f35852a919432b11a6761860bd0db22c6da2600c159ef0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141619"
---
# <a name="updating-assemblies"></a>Atualizando assemblies

As informações neste tópico identificam as diretrizes recomendadas para atualizar assemblies usando patches Windows Instalador.

Os autores de atualizações de assembly podem usar as seguintes diretrizes, que se aplicam a todos os tipos de assemblies:

-   O método recomendado para atualizar um assembly é alterar o nome forte do assembly na [tabela MsiAssemblyName](msiassemblyname-table.md). A nova versão do assembly pode ser fornecida por um novo componente ou pelo mesmo componente que fornece a versão antiga.
-   Se a nova versão do assembly for fornecida pelo mesmo componente, não altere o tipo de assembly de um assembly .NET Framework para um assembly Win32 ou vice-versa.
-   Se todos os aplicativos no sistema devem usar o assembly atualizado, você deve implantar um assembly de política. Um assembly de política pode redirecionar aplicativos no sistema para usar a nova versão do assembly. Assemblies de política devem ser fornecidos criando um novo componente.
-   Windows O instalador 3.0 ou posterior é necessário para desinstalar atualizações de assembly. Para obter mais informações, [consulte Removendo patches](removing-patches.md).
-   A versão mais recente do assembly deve conter as mesmas versões ou versões superiores de arquivos de assemblies lançados anteriormente.
-   Windows O Instalador 3.0 pode .NET Framework assemblies Win32 e .NET Framework por uma substituição de arquivo completa ou por uma atualização delta menor. Para obter mais informações, consulte [Reduzindo o tamanho do patch.](reducing-patch-size.md)
-   Se a atualização mudar o nome forte do assembly, a tabela [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) serão necessárias se o pacote de patch não tiver uma [tabela MsiPatchSequence.](msipatchsequence-table.md) A tabela MsiPatchOldAssemblyFile e a tabela MsiPatchOldAssemblyName não serão necessárias se o pacote de patch tiver informações de sequenciamento de patch em uma tabela MsiPatchSequence.
-   Antes de liberar um novo patch, teste o patch aplicando-o com todos os patches lançados anteriormente.

## <a name="updating-win32-assemblies"></a>Atualizando assemblies win32

Use as seguintes diretrizes ao atualizar assemblies Win32:

-   Altere o nome forte do novo assembly especificado na [tabela MsiAssemblyName](msiassemblyname-table.md).
-   Se você quiser que seu aplicativo sempre use a nova versão do assembly sem afetar a versão do assembly usada por outros aplicativos no sistema, use o mesmo componente para conter a nova versão de assembly usada para a versão antiga do assembly. Mantenha a mesma ComponentId na [tabela Componente.](component-table.md) Depois que o aplicativo é aplicação de patch, ele mantém apenas uma referência à nova versão do assembly. A versão antiga do assembly pode permanecer com a nova versão no cache de assembly global. Isso não afeta outros aplicativos no sistema que usam a versão antiga do assembly. Quando o mesmo componente é usado para as versões novas e antigas do assembly, sua atualização pode ser um patch delta menor.
-   Se a nova versão do assembly não for compatível com todos os sistemas em que você deseja instalar seu aplicativo, você poderá instalar as versões novas e antigas do assembly como assemblies lado a lado. Para instalar as duas versões de assembly lado a lado, crie um novo componente para conter a nova versão do assembly. A ComponentId na tabela [Component](component-table.md) para o novo componente deve ser diferente da ComponentId do componente com a versão antiga. Depois que o aplicativo for a patch, ele manterá referências a ambas as versões de assembly. Em seguida, o aplicativo pode ser direcionado para a versão compatível do assembly por um manifesto. Quando componentes diferentes são usados para as versões novas e antigas do assembly, sua atualização usa a substituição completa de arquivo.

## <a name="updating-net-framework-assemblies"></a>Atualizando .NET Framework assemblies

Use as diretrizes a seguir ao atualizar .NET Framework assemblies.

-   Altere o nome forte do novo assembly especificado na [tabela MsiAssemblyName](msiassemblyname-table.md).
-   Se você quiser que seu aplicativo sempre use a nova versão do assembly sem afetar a versão do assembly usada por outros aplicativos no sistema, altere o nome forte do novo assembly especificado na tabela [MsiAssemblyName](msiassemblyname-table.md)e use o mesmo componente para conter a nova versão de assembly usada para a versão antiga do assembly. Mantenha a mesma ComponentId na [tabela Componente.](component-table.md) Depois que o aplicativo é aplicação de patch, ele mantém apenas uma referência à nova versão do assembly. A versão antiga do assembly pode permanecer com a nova versão no cache global. Isso não afeta outros aplicativos no sistema que usam a versão antiga do assembly. Quando o mesmo componente é usado para as versões novas e antigas do assembly, sua atualização pode ser um patch delta menor.
-   Se a nova versão do assembly não for compatível com todos os sistemas em que você deseja instalar seu aplicativo, você poderá instalar as versões novas e antigas do assembly como assemblies lado a lado. Para instalar as duas versões de assembly lado a lado, altere o nome forte do novo assembly especificado na tabela [MsiAssemblyName](msiassemblyname-table.md)e crie um novo componente para conter a nova versão do assembly. A ComponentId na tabela [Componente](component-table.md) do novo componente deve ser diferente da ComponentId do componente com a versão antiga. Depois que o aplicativo for a patch, ele manterá referências a ambas as versões de assembly. Em seguida, o aplicativo pode ser direcionado para a versão compatível do assembly por um manifesto. Quando componentes diferentes são usados para as versões novas e antigas do assembly, sua atualização usa a substituição completa de arquivo.
-   Uma atualização in-loco substitui a cópia de um assembly .NET Framework no cache de assembly global. Esse tipo de atualização de assembly não altera o nome forte do assembly. Somente o valor no campo FileVersion da [tabela MsiAssemblyName](msiassemblyname-table.md) é alterado. A atualização in-locar de um assembly .NET Framework requer .NET Framework 1.1 SP1 ou superior.
    > [!Note]  
    > O tipo in-loco de atualização substitui a cópia do assembly no cache global e pode quebrar outros aplicativos se a nova versão do assembly não for completamente compatível com versões anteriores. O método recomendado para atualizar um assembly é alterar o nome forte do assembly na [tabela MsiAssemblyName](msiassemblyname-table.md).

     

 

 



