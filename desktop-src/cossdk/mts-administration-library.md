---
description: A biblioteca de administração do MTS fornecida com as interfaces de administração do COM+ fornece compatibilidade com versões anteriores da biblioteca de administração do MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Biblioteca de administração MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500922"
---
# <a name="mts-administration-library"></a>Biblioteca de administração MTS

A biblioteca de administração do MTS fornecida com as interfaces de administração do COM+ fornece compatibilidade com versões anteriores da biblioteca de administração do MTS 2,0. O código de administração do MTS 2,0 mais existente ainda funcionará com a biblioteca MTSAdmin fornecida; no entanto, algumas funcionalidades foram alteradas.

Para aproveitar a nova funcionalidade ou se estiver escrevendo o código de Administração pela primeira vez, você deverá usar a biblioteca COMAdmin.

Os seguintes elementos na biblioteca de administração MTS atual são alterados da biblioteca de administração do MTS 2,0:

-   A interface **IRemoteComponentUtil** não está mais disponível.
-   A coleção **RemoteComponents** não está mais disponível.
-   A Propriedade RoleID não está mais disponível, o nome da função agora é usado como a chave para isso.
-   O método **ExportPackage** não exporta mais um client.exe.
-   A propriedade RemoteComponentInstallPath não é mais exposta na coleção [**LocalComputer**](localcomputer.md) .
-   A propriedade ApplicationInstallPath não será mais exposta na coleção [**LocalComputer**](localcomputer.md) .
-   O pacote do sistema agora é chamado de aplicativo do sistema.
-   O pacote de utilitários agora é chamado de utilitários COM+.
-   A Propriedade IsSystem existe na coleção de [**componentes**](components.md) em MTSAdmin, mas retornará "NotImpl" Quando marcada e não será salva se estiver definida.
-   A Propriedade PackageName não tem mais suporte da coleção de [**componentes**](components.md) . Para descobrir o nome do pacote, agora você precisará obter o PackageID e, em seguida, encontrar o pacote correspondente na coleção de pacotes.
-   As propriedades a seguir não existem mais na coleção [**InterfacesForComponent**](interfacesforcomponent.md) :
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **TypeLibfile**
    -   **TypeLibid**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conversão automática do MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Resultados e problemas de conversão de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversão manual do MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



