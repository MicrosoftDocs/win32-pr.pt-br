---
title: O modelo de caminho de áudio seguro (preterido)
description: O modelo de caminho de áudio seguro (preterido)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- SDK do Windows Media Format, caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro da Microsoft (SAP)
- SDK do Windows Media Format, caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- DRM (gerenciamento de direitos digitais), caminho de áudio seguro (SAP)
- Caminho de áudio seguro da Microsoft (SAP), modelo
- Caminho de áudio seguro (SAP), modelo
- SAP (caminho de áudio seguro), modelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363895"
---
# <a name="the-secure-audio-path-model-deprecated"></a>O modelo de caminho de áudio seguro (preterido)

Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.

O Microsoft Secure áudio Path (SAP) é um recurso do Microsoft Windows® me e do Microsoft Windows XP. O requisito de que um arquivo de áudio seja reproduzido somente por meio de um caminho de áudio seguro é especificado na licença DRM e imposto pelos componentes do cliente DRM. Não há criptografia extra adicional para arquivos somente SAP quando eles são protegidos inicialmente. A criptografia SAP é adicionada automaticamente pelos componentes DRM no momento da reprodução, assim como o processo de autenticação para todos os componentes de software envolvidos na reprodução. Portanto, os funcionamentos do SAP são completamente transparentes para os aplicativos, e é por isso que não há nenhum método ou propriedade no SDK do Windows Media Format para habilitar ou desabilitar o SAP. Se desejar, ao criar um arquivo protegido, um proprietário de conteúdo poderá adicionar um atributo de cabeçalho personalizado chamado algo como "DRMHeader. SAPRequired" para instruir um servidor de licença a adicionar o requisito do SAP à licença. A implementação desse esquema é até o proprietário do conteúdo e o serviço de licença.

No modelo DRM atual, se o SAP não for aplicado, quando música digital protegida for reproduzida, o conteúdo criptografado passará para o componente cliente DRM. O cliente DRM verifica se o aplicativo e o componente DRM que estão incorporando o SDK do Windows Media Format são válidos. Se eles forem válidos, o cliente DRM descriptografará o conteúdo e o enviará para o aplicativo, que o enviará para os componentes de áudio de nível inferior. Neste ponto, a música descriptografada está disponível para aplicativos de modo de usuário, plug-ins e drivers de modo kernel que podem interceptar os bits de áudio descriptografados.

Quando o requisito de caminho de áudio seguro é aplicado, o conteúdo não é descriptografado pelo aplicativo, mas é passado em um estado criptografado para componentes de nível inferior, todos os quais foram autenticados pela Microsoft como confiáveis. Um componente de áudio confiável é aquele que não disponibiliza o conteúdo de áudio para nenhum componente do sistema, exceto outros componentes confiáveis específicos. Dessa forma, o conteúdo digital permanece protegido até o nível do driver.

O diagrama a seguir exibe o modelo atual em comparação com o modelo de caminho de áudio seguro.

![diagrama do modelo de caminho de áudio seguro](images/sap.png)

 

 




