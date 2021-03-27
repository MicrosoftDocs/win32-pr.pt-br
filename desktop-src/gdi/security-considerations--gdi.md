---
description: Este tópico fornece informações sobre considerações de segurança relacionadas ao GDI. Este tópico não fornece tudo o que você precisa saber sobre problemas de segurança. Em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considerações de segurança: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922176"
---
# <a name="security-considerations-gdi"></a>Considerações de segurança: GDI

Este tópico fornece informações sobre considerações de segurança relacionadas ao GDI. Este tópico não fornece tudo o que você precisa saber sobre problemas de segurança. Em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.

A GDI geralmente tem poucas preocupações com a segurança porque lida com exibição em vez de entrada. No entanto, aqui estão alguns problemas que você deve considerar.

Os bitmaps, os metaarquivos e as fontes são estruturas complexas que podem se tornar corrompidas. É uma boa prática tentar garantir que esses itens sejam corrompidos e de uma fonte confiável.

Um aplicativo pode especificar o descritor de segurança para algumas das APIs de impressão e spool. Você deve tomar cuidado ao definir o descritor de segurança.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Central de segurança da Microsoft](https://www.microsoft.com/security/)
</dt> <dt>

[Centro de desenvolvedores de segurança](https://technet.microsoft.com/security/)
</dt> <dt>

[TechCenter de segurança](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



