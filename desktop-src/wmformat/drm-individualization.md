---
title: Individualização de DRM
description: Individualização de DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows SDK de formato de mídia, individualização de DRM
- DRM (gerenciamento de direitos digitais), individualização
- DRM (gerenciamento de direitos digitais), individualização
- individualização do DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16704c968002ee9d9d9cd9a47bf71dd315c2c599848b2ea18b23408ec7a0507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848680"
---
# <a name="drm-individualization"></a>Individualização de DRM

os proprietários de conteúdo protegido podem exigir que os usuários atualizem alguns dos componentes DRM (gerenciamento de direitos digitais) incluídos no SDK do formato de mídia Windows antes de acessar seu conteúdo. Se um usuário aceitar a atualização, uma versão individualizada de um arquivo de segurança (única para seu computador) será baixada de um site da Microsoft. Se o usuário recusar a atualização, não poderá acessar o conteúdo; no entanto, eles ainda poderão acessar conteúdo desprotegido e conteúdo protegido que não exija a atualização. A execução de uma atualização de segurança ajuda a aumentar o nível de proteção oferecido pelo DRM.

A individualização pode ser feita no momento da instalação ou quando um aplicativo encontra primeiro um arquivo ASF protegido que o exige. Como esse processo modifica os componentes do sistema de um usuário, o aplicativo deve notificar o usuário e obter seu consentimento informado antes de executar a atualização. o Microsoft Windows Media Player, por exemplo, mostra uma caixa de diálogo com o seguinte texto:

**Atualização de segurança necessária**

**O proprietário do conteúdo protegido que você está tentando acessar requer primeiro a atualização de alguns dos componentes do Microsoft DRM (gerenciamento de direitos digitais) em seu computador.**

**Clique em OK para atualizar seus componentes DRM.**

**Ver**

**Quando você clica em OK, um identificador exclusivo e um arquivo de segurança DRM são enviados a um serviço da Microsoft na Internet. O arquivo é substituído por uma versão personalizada que contém seu identificador exclusivo. Isso aumenta o nível de proteção fornecido pelo DRM.**

Qualquer aplicativo que dê suporte à individualização deve usar o mesmo texto ou uma palavra semelhante. Para obter mais informações sobre a política de privacidade da Microsoft, consulte a seção [declaração de privacidade](privacy-statement.md) desta documentação.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Individualizando aplicativos DRM**](individualizing-drm-applications.md)
</dt> </dl>

 

 




