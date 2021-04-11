---
title: Fazendo backup e restaurando licenças DRM
description: Fazendo backup e restaurando licenças DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- SDK do Windows Media Format, fazendo backup de licenças DRM
- SDK do Windows Media Format, restaurando licenças DRM
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- SDK do Windows Media Format, recurso de restauração de backup
- SDK do Windows Media Format, serviço de gerenciamento de licenças
- SDK do Windows Media Format, detecção de fraudes
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), recurso de restauração de backup
- DRM (gerenciamento de direitos digitais), recurso de restauração de backup
- DRM (gerenciamento de direitos digitais), serviço de gerenciamento de licenças
- DRM (gerenciamento de direitos digitais), serviço de gerenciamento de licenças
- DRM (gerenciamento de direitos digitais), detecção de fraudes
- DRM (gerenciamento de direitos digitais), detecção de fraudes
- fazendo backup de licenças DRM
- restaurando licenças DRM
- licenças, DRM
- licenças, fazendo backup de DRM
- licenças, restaurando DRM
- Recurso de restauração de backup
- Serviço de gerenciamento de licenças
- detecção de fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104294565"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a>Fazendo backup e restaurando licenças DRM

Com o recurso de restauração de backup, os usuários podem fazer backup e restaurar [*licenças*](wmformat-glossary.md) no mesmo computador ou em outros computadores. Esse recurso permite que os usuários transfiram licenças para um novo computador ou de volta para o mesmo computador (depois de reformatar o disco rígido, por exemplo). Além disso, os usuários podem reproduzir arquivos ASF protegidos em mais de um computador.

Para incentivar o uso legítimo de uma licença, uma política de detecção de fraude restringe o número de vezes que uma licença pode ser restaurada. A Microsoft fornece um serviço que controla o número de computadores para os quais uma licença foi restaurada; se um limite for atingido, o usuário não poderá restaurar a licença.

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a>Permitir ou não permitir o direito de fazer backup e restaurar

O recurso de restauração de backup funciona apenas para licenças para as quais o direito de backup e restauração é fornecido. Se os proprietários de conteúdo ou os emissores de licença não quiserem esse recurso, ou se eles emitirem licenças que contenham um estado seguro (como operações contadas ou tempo limitado), eles poderão não permitir esse direito.

Quando uma licença não pode ser restaurada porque um usuário não tem o direito, uma [*ID de chave*](wmformat-glossary.md) é passada para o aplicativo. No mínimo, o usuário deve ser notificado de que não foi possível fazer o backup de algumas licenças, embora o usuário não saiba a quais licenças essa mensagem se refere. Se você souber a ID da chave para arquivos protegidos disponíveis, poderá desenvolver uma solução mais robusta para informar o usuário.

Por exemplo, um player poderia ser desenvolvido para um rótulo de registro que fornece músicas protegidas na Internet. Essas músicas e suas IDs de chave podem ser rastreadas em um banco de dados. Se não for possível fazer backup de algumas licenças, o aplicativo de Player poderá usar a ID de chave para consultar o banco de dados para o nome das músicas e informar ao usuário para quais músicas não é possível fazer backup das licenças. Ou, uma biblioteca de música pode ser criada para cada usuário localmente e a ID da chave pode ser usada para recuperar mais informações sobre quais licenças não puderam ser submetidas a backup.

## <a name="the-license-management-service"></a>O serviço de gerenciamento de licenças

Quando o recurso de restauração de backup é implementado, um serviço de gerenciamento de licenças hospedado pela Microsoft gerencia a restauração de licenças.

Primeiro, os usuários fazem backup de licenças no aplicativo, por exemplo, escolhendo uma opção de menu. Todas as licenças no computador são submetidas a backup em um local especificado, como um disquete. Em seguida, os usuários restauram licenças usando o aplicativo, por exemplo, escolhendo uma opção de menu e especificando seu local de backup.

Neste ponto, o usuário deve estar conectado à Internet; uma solicitação do aplicativo é enviada para o serviço de gerenciamento de licenças. Se o computador do qual foi feito o backup da licença for diferente do computador original (ou se o computador original tiver sido reformatado), o serviço de gerenciamento de licenças emitirá uma nova licença para o novo computador. Caso contrário, a licença que foi emitida anteriormente para esse computador será reemitida.

Como o serviço de gerenciamento de licenças recupera informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no [site da Microsoft](https://www.microsoft.com/licensing/default).

> [!Note]  
> Quando um usuário final restaura uma licença para um computador diferente e a licença requer individualização, o usuário final deve autorizar os componentes DRM a serem atualizados. Você deve implementar um processo em seu aplicativo de Player para dar suporte a esse recurso.

 

## <a name="detecting-fraud"></a>Detectando fraude

O usuário tem permissão para restaurar uma licença por um número limitado de vezes. Cada vez que uma licença é restaurada, o serviço de gerenciamento de licenças a acompanha e incrementa a contagem dessa licença em uma. Ao restaurar uma licença para um computador no qual a licença foi restaurada anteriormente (por exemplo, o computador do qual foi feito o backup da licença), a contagem não é aumentada. Um computador é considerado diferente se tiver um novo sistema operacional ou se o sistema operacional tiver sido reinstalado.

De acordo com a política de detecção de fraudes da Microsoft, quando uma licença é restaurada um determinado número de vezes, o aplicativo recebe uma URL dos componentes do DRM e é responsável por abrir um navegador e exibir a página da Web, o que indica que o contrato de licença pode ter sido violado. O usuário deve entrar em contato com o distribuidor de licenças, que deve determinar se a solicitação é válida.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Fazendo backup e restaurando licenças**](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




