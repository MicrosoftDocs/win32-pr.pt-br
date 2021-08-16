---
title: Fazer o back-up e a restauração de licenças DRM
description: Fazer o back-up e a restauração de licenças DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows SDK de Formato de Mídia, fazer o back-up de licenças DRM
- Windows SDK de Formato de Mídia, restaurando licenças DRM
- Windows SDK de Formato de Mídia, licenças DRM
- Windows SDK de Formato de Mídia, licenças para DRM
- Windows SDK de Formato de Mídia, Recurso de Restauração de Backup
- Windows SDK de Formato de Mídia, Serviço de Gerenciamento de Licenças
- Windows SDK de Formato de Mídia, detecção de fraudes
- DRM (gerenciamento de direitos digitais), fazer o back-up de licenças
- DRM (gerenciamento de direitos digitais), fazer o back-up de licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), recurso de restauração de backup
- DRM (gerenciamento de direitos digitais), recurso de restauração de backup
- DRM (gerenciamento de direitos digitais), Serviço de Gerenciamento de Licenças
- DRM (gerenciamento de direitos digitais), Serviço de Gerenciamento de Licenças
- DRM (gerenciamento de direitos digitais), detecção de fraudes
- DRM (gerenciamento de direitos digitais), detecção de fraudes
- fazer o back-up de licenças drm
- restaurando licenças DRM
- licenças, DRM
- licenças, fazer o back-up do DRM
- licenças, restaurando DRM
- Recurso de restauração de backup
- Serviço de Gerenciamento de Licenças
- detecção de fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019163a42312b14b7d7b7e15cea68be1996a976e42b31491f62486a43d37b8bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028144"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Fazer o back-up e a restauração de licenças DRM

Com o recurso Restauração de Backup, os usuários podem fazer backup e restaurar [*licenças*](wmformat-glossary.md) no mesmo computador ou em outros computadores. Esse recurso permite que os usuários transfiram licenças para um novo computador ou de volta para o mesmo computador (depois de reformatar o disco rígido, por exemplo). Além disso, os usuários podem reproduzir arquivos ASF protegidos em mais de um computador.

Para incentivar o uso legítimo de uma licença, uma política de detecção de fraudes restringe o número de vezes que uma licença pode ser restaurada. A Microsoft fornece um serviço que rastreia o número de computadores para os quais uma licença foi restaurada; se um limite for atingido, o usuário não poderá restaurar a licença.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Permitindo ou não permitindo o direito de fazer backup e restaurar

O recurso Restauração de Backup funciona apenas para licenças para as quais o direito backup e restauração é dado. Se os proprietários de conteúdo ou emissores de licença não quiserem esse recurso ou se emitirem licenças que contenham um estado seguro (como operações contadas ou tempo limitado), eles poderão não permitir esse direito.

Quando uma licença não pode ser restaurada porque um usuário não tem o direito, uma [*ID de chave*](wmformat-glossary.md) é passada para o aplicativo. No mínimo, o usuário deve ser notificado de que não foi possível fazer backup de algumas licenças, embora o usuário não saiba a quais licenças essa mensagem se refere. Se você conhecer a ID de chave para arquivos protegidos disponíveis, poderá desenvolver uma solução mais robusta para informar o usuário.

Por exemplo, um player pode ser desenvolvido para um rótulo de registro que fornece músicas protegidas na Internet. Essas músicas e suas IDs de chave podem ser rastreadas em um banco de dados. Se não for possível fazer backup de algumas licenças, o aplicativo player poderá usar a ID da chave para consultar o nome das músicas no banco de dados e, em seguida, informar ao usuário para quais músicas as licenças não podem ser apoiadas. Ou, uma biblioteca de música pode ser criada para cada usuário localmente e a ID da chave pode ser usada para recuperar mais informações sobre quais licenças não puderam ser recuperadas.

## <a name="the-license-management-service"></a>O Serviço de Gerenciamento de Licenças

Quando o recurso restauração de backup é implementado, um Serviço de Gerenciamento de Licenças hospedado pela Microsoft gerencia a restauração de licenças.

Primeiro, os usuários podem fazer o back-up de licenças no aplicativo, por exemplo, escolhendo uma opção de menu. Todas as licenças no computador têm o backup feito em um local especificado, como um disquete. Em seguida, os usuários restauram licenças usando o aplicativo, por exemplo, escolhendo uma opção de menu e especificando seu local de backup.

Neste ponto, o usuário deve estar conectado à Internet; uma solicitação do aplicativo é enviada para o Serviço de Gerenciamento de Licenças. Se o computador do qual foi feito o backup da licença for diferente do computador original (ou se o computador original tiver sido reformatado), o Serviço de Gerenciamento de Licenças emite uma nova licença para o novo computador. Caso contrário, a licença que foi emitida anteriormente para esse computador será emitida.

Como o Serviço de Gerenciamento de Licenças recupera informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no [site da Microsoft.](https://www.microsoft.com/licensing/default)

> [!Note]  
> Quando um usuário final restaura uma licença para um computador diferente e a licença requer individualização, o usuário final deve autorizar os componentes do DRM a serem atualizados. Você deve implementar um processo em seu aplicativo de player para dar suporte a esse recurso.

 

## <a name="detecting-fraud"></a>Detectando fraudes

O usuário tem permissão para restaurar uma licença um número limitado de vezes. Sempre que uma licença é restaurada, o Serviço de Gerenciamento de Licenças a rastreia e incrementa a contagem dessa licença em um. Ao restaurar uma licença em um computador no qual a licença foi restaurada anteriormente (por exemplo, o computador do qual a licença foi backup), a contagem não é aumentada. Um computador será considerado diferente se tiver um novo sistema operacional ou se o sistema operacional tiver sido instalado.

De acordo com a política de detecção de fraudes da Microsoft, quando uma licença é restaurada um determinado número de vezes, o aplicativo recebe uma URL dos componentes drm e é responsável por abrir um navegador e exibir a página da Web, o que indica que o contrato de licença pode ter sido violado. O usuário deve entrar em contato com o distribuidor de licenças, que deve determinar se a solicitação é válida.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Fazer o back-up e restaurar licenças**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




