---
description: As informações neste tópico identificam as diretrizes recomendadas para a atualização de assemblies usando patches de Windows Installer.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Atualizando assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b185a9943ba20c81a1fa3431dd590eb05648c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011841"
---
# <a name="updating-assemblies"></a>Atualizando assemblies

As informações neste tópico identificam as diretrizes recomendadas para a atualização de assemblies usando patches de Windows Installer.

Os autores de atualizações de assembly podem usar as seguintes diretrizes, que se aplicam a todos os tipos de assemblies:

-   O método recomendado para atualizar um assembly é alterar o nome forte do assembly na [tabela MsiAssemblyName](msiassemblyname-table.md). A nova versão do assembly pode ser fornecida por um novo componente ou pelo mesmo componente que fornece a versão antiga.
-   Se a nova versão do assembly for fornecida pelo mesmo componente, não altere o tipo de assembly de um assembly .NET Framework para um assembly Win32 ou vice-versa.
-   Se todos os aplicativos no sistema precisarem usar o assembly atualizado, você deverá implantar um assembly de política. Um assembly de política pode redirecionar aplicativos no sistema para usar a nova versão do assembly. Os assemblies de política devem ser fornecidos pela criação de um novo componente.
-   Windows Installer 3,0 ou posterior é necessário para desinstalar as atualizações de assembly. Para obter mais informações, consulte [removendo patches](removing-patches.md).
-   A versão mais recente do assembly deve conter as mesmas ou versões mais recentes de arquivos de assemblies lançados anteriormente.
-   Windows Installer 3,0 pode atender a assemblies de .NET Framework e do Win32 por uma substituição de arquivo completa ou por uma atualização Delta menor. Para obter mais informações, consulte [reduzindo o tamanho do patch](reducing-patch-size.md).
-   Se a atualização alterar o nome forte do assembly, a tabela [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e a tabela [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) serão necessárias se o pacote de patch não tiver uma tabela [MsiPatchSequence](msipatchsequence-table.md) . A tabela MsiPatchOldAssemblyFile e a tabela MsiPatchOldAssemblyName não serão necessárias se o pacote de patch tiver informações de sequenciamento de patch em uma tabela MsiPatchSequence.
-   Antes de liberar um novo patch, teste o patch aplicando-o a todos os patches lançados anteriormente.

## <a name="updating-win32-assemblies"></a>Atualizando assemblies do Win32

Use as seguintes diretrizes ao atualizar assemblies do Win32:

-   Altere o nome forte do novo assembly que é especificado na [tabela MsiAssemblyName](msiassemblyname-table.md).
-   Se você quiser que seu aplicativo sempre use a nova versão do assembly sem afetar a versão do assembly usada por outros aplicativos no sistema, use o mesmo componente para conter a nova versão do assembly que você usou para a versão antiga do assembly. Mantenha o mesmo ComponentID na tabela de [componentes](component-table.md) . Depois que o aplicativo é corrigido, ele só mantém uma referência à nova versão do assembly. A versão antiga do assembly pode permanecer com a nova versão no cache de assembly global. Isso não afeta outros aplicativos no sistema que usam a versão antiga do assembly. Quando o mesmo componente é usado para as versões novas e antigas do assembly, sua atualização pode ser um patch Delta menor.
-   Se a nova versão do assembly não for compatível com todos os sistemas nos quais você deseja instalar o aplicativo, você poderá instalar as versões novas e antigas do assembly como assemblies lado a lado. Para instalar as duas versões do assembly lado a lado, crie um novo componente para conter a nova versão do assembly. O ComponentID na tabela de [componentes](component-table.md) para o novo componente deve ser diferente do ComponentID do componente com a versão antiga. Depois que o aplicativo é corrigido, ele mantém referências a ambas as versões do assembly. Em seguida, o aplicativo pode ser direcionado para a versão compatível do assembly por um manifesto. Quando componentes diferentes são usados para as versões novas e antigas do assembly, sua atualização usa a substituição de arquivo completa.

## <a name="updating-net-framework-assemblies"></a>Atualizando assemblies de .NET Framework

Use as diretrizes a seguir ao atualizar .NET Framework assemblies.

-   Altere o nome forte do novo assembly que é especificado na [tabela MsiAssemblyName](msiassemblyname-table.md).
-   Se você quiser que seu aplicativo sempre use a nova versão do assembly sem afetar a versão do assembly usada por outros aplicativos no sistema, altere o nome forte do novo assembly especificado na [tabela MsiAssemblyName](msiassemblyname-table.md)e use o mesmo componente para conter a nova versão do assembly que você usou para a versão antiga do assembly. Mantenha o mesmo ComponentID na tabela de [componentes](component-table.md) . Depois que o aplicativo é corrigido, ele só mantém uma referência à nova versão do assembly. A versão antiga do assembly pode permanecer com a nova versão no cache global. Isso não afeta outros aplicativos no sistema que usam a versão antiga do assembly. Quando o mesmo componente é usado para as versões novas e antigas do assembly, sua atualização pode ser um patch Delta menor.
-   Se a nova versão do assembly não for compatível com todos os sistemas nos quais você deseja instalar o aplicativo, você poderá instalar as versões novas e antigas do assembly como assemblies lado a lado. Para instalar as duas versões do assembly lado a lado, altere o nome forte do novo assembly especificado na [tabela MsiAssemblyName](msiassemblyname-table.md)e crie um novo componente para conter a nova versão do assembly. O ComponentID na tabela de [componentes](component-table.md) para o novo componente deve ser diferente do componenteid do componente com a versão antiga. Depois que o aplicativo é corrigido, ele mantém referências a ambas as versões do assembly. O aplicativo pode ser direcionado para a versão compatível do assembly por um manifesto. Quando componentes diferentes são usados para as versões novas e antigas do assembly, sua atualização usa a substituição de arquivo completa.
-   Uma atualização in-loco substitui a cópia de um assembly .NET Framework no cache de assembly global. Esse tipo de atualização de assembly não altera o nome forte do assembly. Somente o valor no campo FileVersion da [tabela MsiAssemblyName](msiassemblyname-table.md) é alterado. A atualização in-loco de um assembly .NET Framework requer o .NET Framework 1,1 SP1 ou superior.
    > [!Note]  
    > O tipo de atualização in-loco substitui a cópia do assembly no cache global e pode interromper outros aplicativos se a nova versão do assembly não for totalmente compatível com versões anteriores. O método recomendado para atualizar um assembly é alterar o nome forte do assembly na [tabela MsiAssemblyName](msiassemblyname-table.md).

     

 

 



