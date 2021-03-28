---
description: Funções de notificação
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Funções de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091463"
---
# <a name="notification-functions"></a>Funções de notificação



| Função Flat                                                                  | Método de wrapper                            | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook (saída \_ token ULONG PTR \* )<br/> | Não chamado por métodos de wrapper.<br/> | A função [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) retorna (em seu parâmetro de saída) um ponteiro para uma estrutura [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . Um dos membros da estrutura é um ponteiro para uma função de gancho de notificação que tem a mesma assinatura que GdiplusNotificationHook.<br/> Há duas maneiras de chamar a função de gancho de notificação; Você pode usar o ponteiro retornado por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) ou pode chamar GdiplusNotificationHook. Na verdade, GdiplusNotificationHook simplesmente verifica se você eliminou o thread em segundo plano e, em seguida, chama a função de gancho de notificação retornada pelo **GdiplusStartup**.<br/> O parâmetro token recebe um identificador que você deve passar posteriormente em uma chamada correspondente para a função de desconexão de notificação.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook (token do ULONG \_ PTR)<br/>         | Não chamado por métodos de wrapper.<br/> | A função [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) retorna (em seu parâmetro de saída) um ponteiro para uma estrutura [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . Um dos membros da estrutura é um ponteiro para uma função de desconexão de notificação que tem a mesma assinatura que GdiplusNotificationUnhook.<br/> Há duas maneiras de chamar a função de desconexão de notificação; Você pode usar o ponteiro retornado por [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) ou pode chamar GdiplusNotificationUnhook. Na verdade, GdiplusNotificationUnhook simplesmente verifica se você eliminou o thread em segundo plano e, em seguida, chama a função de desconexão de notificação retornada por **GdiplusStartup**.<br/> Quando você chamar a função de desconexão de notificação, passe o token que você recebeu anteriormente de uma chamada correspondente para a função de gancho de notificação. Se você não fizer isso, haverá vazamentos de recursos que não serão limpos até que o processo saia.<br/> |



 

 

 




