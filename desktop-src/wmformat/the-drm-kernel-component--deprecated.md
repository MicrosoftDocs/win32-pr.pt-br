---
title: O componente de kernel do DRM (preterido)
description: O componente de kernel do DRM (preterido)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows SDK do formato de mídia, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- Windows SDK do formato de mídia, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- Windows SDK do formato de mídia, componente do kernel do DRM
- DRM (gerenciamento de direitos digitais), componente de kernel
- DRM (gerenciamento de direitos digitais), componente de kernel
- Caminho de áudio seguro da Microsoft (SAP), componente de kernel do DRM
- Caminho de áudio seguro (SAP), componente de kernel do DRM
- SAP (caminho de áudio seguro), componente de kernel do DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8db4389d9156ef13d9e87983a4ae433e6028805268f3cbd55690d4d0d8144b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845753"
---
# <a name="the-drm-kernel-component-deprecated"></a>O componente de kernel do DRM (preterido)

Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.

No modelo de caminho de áudio seguro da Microsoft (SAP), o componente de kernel do DRM fornece dois recursos básicos que protegem a integridade de músicas criptografadas.

Primeiro, o componente de cliente DRM e o componente de kernel DRM estão em comunicação quando um arquivo de música é reproduzido. Essa comunicação entre os componentes impede que alguém viole o sinal criptografado ou insira informações falsas.

Em segundo lugar, o componente do kernel do DRM não descriptografa o sinal de música até que todos os componentes restantes sejam autenticados. Ou seja, antes de descriptografar o conteúdo e passá-lo para o próximo componente do sistema, o componente do kernel DRM verifica cada componente que permanece no caminho para a placa de som (cada componente que pode acessar o conteúdo) e verifica se esses componentes estão assinados com um certificado da Microsoft. Um componente não assinado pode indicar um componente suspeito ou um driver mal-intencionado. Assim, quando o componente de kernel DRM valida os componentes restantes, se algum componente falhar nesse teste, o sinal será interrompido e não poderá ser reproduzido. Caso contrário, se todos os componentes passarem na validação, o componente do kernel DRM descriptografará a música e a passará para o próximo componente.

a Microsoft assina digitalmente os drivers que passam os testes de Windows® laboratório de qualidade de Hardware (WHQL) para garantir que os usuários estejam usando os drivers de qualidade mais alta. Essa prática é padrão e garante a autenticidade dos componentes, pois a assinatura não pode ser forjada, nem o código pode ser modificado sem destruir a assinatura. Os drivers que são certificados para o caminho de áudio seguro devem proteger os dados de áudio que eles processam do acesso por componentes não confiáveis. 

os Drivers incluídos no Windows Millennium Edition e Windows XP são atualizados para proteger o caminho de áudio e assinados. Drivers que não são assinados para uso com Windows Me ou Windows XP não podem reproduzir música protegida. Os fabricantes de driver podem reemitir versões atualizadas de seus drivers assinados pelo WHQL e publicá-las na Internet para que os consumidores baixem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Caminho de áudio seguro da Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




