---
title: O componente de kernel do DRM (preterido)
description: O componente de kernel do DRM (preterido)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- SDK do Windows Media Format, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- SDK do Windows Media Format, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- SDK do Windows Media Format, componente do kernel do DRM
- DRM (gerenciamento de direitos digitais), componente de kernel
- DRM (gerenciamento de direitos digitais), componente de kernel
- Caminho de áudio seguro da Microsoft (SAP), componente de kernel do DRM
- Caminho de áudio seguro (SAP), componente de kernel do DRM
- SAP (caminho de áudio seguro), componente de kernel do DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008580"
---
# <a name="the-drm-kernel-component-deprecated"></a>O componente de kernel do DRM (preterido)

Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.

No modelo de caminho de áudio seguro da Microsoft (SAP), o componente de kernel do DRM fornece dois recursos básicos que protegem a integridade de músicas criptografadas.

Primeiro, o componente de cliente DRM e o componente de kernel DRM estão em comunicação quando um arquivo de música é reproduzido. Essa comunicação entre os componentes impede que alguém viole o sinal criptografado ou insira informações falsas.

Em segundo lugar, o componente do kernel do DRM não descriptografa o sinal de música até que todos os componentes restantes sejam autenticados. Ou seja, antes de descriptografar o conteúdo e passá-lo para o próximo componente do sistema, o componente do kernel DRM verifica cada componente que permanece no caminho para a placa de som (cada componente que pode acessar o conteúdo) e verifica se esses componentes estão assinados com um certificado da Microsoft. Um componente não assinado pode indicar um componente suspeito ou um driver mal-intencionado. Assim, quando o componente de kernel DRM valida os componentes restantes, se algum componente falhar nesse teste, o sinal será interrompido e não poderá ser reproduzido. Caso contrário, se todos os componentes passarem na validação, o componente do kernel DRM descriptografará a música e a passará para o próximo componente.

A Microsoft assina digitalmente os drivers que passam os testes do WHQL (laboratório de qualidade de hardware) do Windows® para garantir que os usuários estejam usando os drivers de qualidade mais alta. Essa prática é padrão e garante a autenticidade dos componentes, pois a assinatura não pode ser forjada, nem o código pode ser modificado sem destruir a assinatura. Os drivers que são certificados para o caminho de áudio seguro devem proteger os dados de áudio que eles processam do acesso por componentes não confiáveis. 

Os drivers incluídos no Windows Millennium Edition e no Windows XP são atualizados para um caminho de áudio seguro e assinados. Os drivers que não estão assinados para uso com o Windows me ou o Windows XP não podem reproduzir música protegida. Os fabricantes de driver podem reemitir versões atualizadas de seus drivers assinados pelo WHQL e publicá-las na Internet para que os consumidores baixem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Caminho de áudio seguro da Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




