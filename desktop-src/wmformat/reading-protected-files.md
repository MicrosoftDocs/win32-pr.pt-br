---
title: Lendo arquivos protegidos
description: Lendo arquivos protegidos
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK, lendo arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), lendo arquivos protegidos
- ASF (formato de sistemas avançados), lendo arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, lendo arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640123"
---
# <a name="reading-protected-files"></a>Lendo arquivos protegidos

Ler um arquivo protegido por DRM ou um fluxo de rede basicamente envolve a tentativa de abrir o arquivo (ou conectar-se ao fluxo) e, em seguida, manipular quaisquer eventos que possam ser enviados dos componentes DRM.

Se um player não estiver habilitado para DRM (não vincula a uma biblioteca wmstubdrm. lib válida), a chamada [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) falhará ao tentar abrir um arquivo protegido e retornará o conteúdo protegido do NS e \_ \_ \_ ou algum erro relacionado.

Quando um aplicativo habilitado para DRM tenta abrir um arquivo protegido por DRM, o componente DRM pesquisa automaticamente o sistema local em busca de uma licença válida. Se um for encontrado, o componente DRM descriptografará automaticamente o arquivo de forma que seja completamente transparente para o aplicativo. A ação que um aplicativo pode executar no arquivo descriptografado depende dos direitos especificados na licença. Para obter uma descrição completa dos possíveis direitos, consulte a documentação do SDK do Windows Media Rights Manager.

Se o aplicativo não tiver uma licença válida para um arquivo, o Player receberá uma notificação de status do componente DRM. O aplicativo de player pode iniciar o processo de [*aquisição de licença*](wmformat-glossary.md) . Depois que uma licença válida tiver sido recebida, o arquivo poderá ser acessado. As seções a seguir descrevem as tarefas básicas que um aplicativo deve executar ao implementar o processo de aquisição de licença:

-   [Especificando as ações a serem executadas](specifying-the-actions-to-be-performed.md)
-   [Lidando com eventos de aquisição de licença](handling-license-acquisition-events.md)
-   [Individualizando aplicativos DRM](individualizing-drm-applications.md)
-   [Manipulando eventos de individualização](handling-individualization-events.md)

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




