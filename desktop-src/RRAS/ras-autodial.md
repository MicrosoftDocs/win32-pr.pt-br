---
title: Discagem automática de RAS
description: Um recurso chamado \ 0034; conexão padrão \ 0034; foi adicionado ao sistema no Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Discagem automática, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7956148919505eb16d1fb2fe9bc045fa7ecbaa7e2959c430e15f8013ef372ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909866"
---
# <a name="ras-autodial"></a>Discagem automática de RAS

um recurso chamado "conexão padrão" foi adicionado ao sistema no Windows XP. Se houver uma falha na tentativa de conexão, o sistema verificará se há uma correspondência explícita (para nome do Winsock ou nome do compartilhamento) no banco de dados, se não, ele discará a conexão padrão se houver uma.

**Windows 2000:** Quando uma tentativa de conexão com um endereço de rede falha porque o host não pode ser acessado, o recurso de discagem automática pode iniciar automaticamente uma operação de conexão discada. Para fazer isso, a discagem automática pesquisa seu banco de dados de endereços de rede para localizar uma entrada de catálogo telefônico que pode ser usada para estabelecer a conexão.

* * Windows NT 4,0: * * o RAS mantém um banco de dados dos nomes do Winsock e/ou nomes de compartilhamento que você atingiu com êxito enquanto uma conexão RAS/VPN estava ativa. Posteriormente, quando uma tentativa de conexão Winsock ou compartilhar falha, o sistema verifica esse banco de dados e oferece para discar a conexão armazenada para você.

 

 




