---
description: A função ExcludeUpdateRgn exclui a região de atualização da região de recorte para o contexto do dispositivo de vídeo.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Excluindo a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010730"
---
# <a name="excluding-the-update-region"></a>Excluindo a região de atualização

A função [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) exclui a região de atualização da região de recorte para o contexto do dispositivo de vídeo. Essa função é útil ao desenhar em uma janela diferente de quando uma mensagem do WM \_ Paint está sendo processada. Ele impede o desenho nas áreas que serão atualizadas durante a próxima mensagem do WM \_ Paint.

 

 



