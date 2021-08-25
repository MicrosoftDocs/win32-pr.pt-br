---
title: Caminho de Áudio Seguro da Microsoft (preterido)
description: Caminho de Áudio Seguro da Microsoft (preterido)
ms.assetid: 55833ca4-b25b-408c-af66-f89e9b6110c9
keywords:
- Windows SDK de Formato de Mídia, SAP (Caminho de Áudio Seguro da Microsoft)
- DRM (gerenciamento de direitos digitais), SAP (Caminho de Áudio Seguro da Microsoft)
- DRM (gerenciamento de direitos digitais), SAP (Caminho de Áudio Seguro da Microsoft)
- Windows SDK de formato de mídia, SAP (Caminho de Áudio Seguro)
- DRM (gerenciamento de direitos digitais), SAP (Secure Audio Path)
- DRM (gerenciamento de direitos digitais), SAP (Secure Audio Path)
- SAP (Caminho de Áudio Seguro da Microsoft), sobre
- SAP (Caminho de Áudio Seguro), sobre
- SAP (Caminho de Áudio Seguro),sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17ad44484f99c6a1497511d7c91541a6ad62c184b81b82117cf1d6869038145c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839476"
---
# <a name="microsoft-secure-audio-path-deprecated"></a>Caminho de Áudio Seguro da Microsoft (preterido)

Esta página documenta um recurso que terá suporte com uma solução técnica diferente em versões futuras do Windows.

Criadores de conteúdo e distribuidores podem especificar em uma licença DRM que um arquivo de áudio só tem permissão para ser tocado em um sistema com componentes SAP (Caminho de Áudio Seguro da Microsoft). O Caminho de Áudio Seguro fornece um grau muito mais alto de proteção ao conteúdo de áudio, tornando praticamente impossível que aplicativos ou drivers de áudio não seguros acessem os bits de áudio não criptografados. Há suporte para o Secure Audio Path no Microsoft Windows® Me e Windows XP. Ele garante música digital no kernel do sistema operacional. Além disso, o Digital Copyright Act torna o desviamento de medidas antiabósticas no software como um crime.

O Secure Audio Path é ativado e implementado completamente automaticamente pelo componente DRM da Microsoft quando uma licença drm requer SAP. Para aplicativos em execução no Windows® XP Service Pack 1, você pode habilitar a criptografia SAP para qualquer conteúdo de áudio, fora do contexto da solução drm da Microsoft, usando o SDK do Caminho de Áudio Seguro. Para obter mais informações sobre o SDK do Caminho de Áudio Seguro, consulte o [site da Microsoft](/documentation/).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos Rights Management digital**](digital-rights-management-features.md)
</dt> </dl>

 

 