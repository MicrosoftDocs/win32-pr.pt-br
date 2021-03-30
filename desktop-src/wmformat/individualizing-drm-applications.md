---
title: Individualizando aplicativos DRM
description: Individualizando aplicativos DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- SDK do Windows Media Format, individualizando aplicativos DRM
- Windows Media Format SDK, individualização de aplicativos
- ASF (Advanced Systems Format), individualizando aplicativos DRM
- ASF (formato de sistemas avançados), individualizando aplicativos DRM
- Formato de sistema avançado (ASF), individualização de aplicativo
- ASF (formato de sistemas avançados), individualização de aplicativos
- DRM (gerenciamento de direitos digitais), individualizando aplicativos
- DRM (gerenciamento de direitos digitais), individualizando aplicativos
- DRM (gerenciamento de direitos digitais), individualização de aplicativos
- DRM (gerenciamento de direitos digitais), individualização de aplicativos
- individualização do aplicativo
- individualizando aplicativos DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103917060"
---
# <a name="individualizing-drm-applications"></a>Individualizando aplicativos DRM

Para aumentar a segurança, o componente DRM dos aplicativos pode ser *individualizado*. Um aplicativo individual é aquele que recebeu uma atualização para seus componentes DRM que o diferencia de todas as outras cópias do mesmo aplicativo. Os proprietários de conteúdo podem exigir que seus arquivos protegidos sejam reproduzidos somente em um aplicativo que tenha sido individualizado.

O processo de individualização é iniciado quando o aplicativo entra em contato com o serviço de individualização da Microsoft, que instala uma atualização de segurança no computador do usuário. Como o serviço de individualização manipula informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no site da Microsoft: <https://privacy.microsoft.com/privacystatement> .

A individualização pode ser realizada de maneiras diferentes. Por exemplo, a individualização pode ocorrer quando um usuário reproduz um arquivo protegido. A solicitação de licença é enviada para o [*serviço de licença do Windows Media*](wmformat-glossary.md), que inspeciona o certificado do aplicativo que está solicitando a [*licença*](wmformat-glossary.md). Se o componente DRM do aplicativo não tiver sido individualizado, o serviço de licença do Windows Media se recusará a emitir a licença, pois é a política do serviço de licença do Windows Media para emitir licenças somente para jogadores individualizados. Em seguida, o aplicativo pode notificar o usuário de que o aplicativo deve ser atualizado. Se o usuário concordar, uma atualização de segurança será fornecida para individualizar o componente DRM do aplicativo.

Para uma melhor experiência do usuário, você pode iniciar o processo de individualização como uma etapa de atualização de segurança durante a instalação; em seguida, o usuário não é interrompido para obter uma atualização de segurança ao tentar reproduzir um arquivo protegido. Você também pode incentivar a individualização de forma ativa adicionando um comando de menu de **atualização de segurança** ou um botão ao aplicativo.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




