---
title: Reprodução de áudio simples
description: Reprodução de áudio simples
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- áudio de multimídia, onda
- áudio, onda
- áudio de forma de onda, reprodução simples
- Função MessageBeep
- função sndPlaySound
- Função PlaySound, reprodução simples
- áudio de multimídia, função PlaySound
- áudio, função PlaySound
- áudio de onda, função PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917224"
---
# <a name="simple-audio-playback"></a>Reprodução de áudio simples

Você pode usar as seguintes funções para reproduzir áudio de onda em seu aplicativo em uma única chamada de função.



| Função                                                      | Descrição                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Reproduz o som que corresponde a um nível de alerta de sistema especificado.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Reproduz o som que corresponde ao som do sistema inserido no registro ou ao conteúdo do arquivo especificado. |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | Fornece toda a funcionalidade do [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e pode acessar diretamente os recursos.           |



 

A função **MessageBeep** é uma parte padrão da API do Win32; como suas funcionalidades são muito limitadas e estão documentadas em outro lugar, elas não são discutidas aqui.

As funções listadas dão suporte às seguintes fontes de áudio de formato de onda:

-   Formato de onda-arquivos de áudio associados ao sistema-níveis de alerta
-   Formato de onda-arquivos de áudio especificados por entradas no registro
-   Recursos de onda na memória
-   Formato de onda-arquivos de áudio especificados por nome

As funções [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e [**PlaySound**](/previous-versions//dd743680(v=vs.85)) carregam um arquivo de wave-áudio inteiro na memória e, em vigor, limitam o tamanho do arquivo que eles podem reproduzir. Use **sndPlaySound** e **PlaySound** para reproduzir arquivos de wave-áudio pequenos – até cerca de 100 mil. Essas duas funções também exigem que os dados de som estejam em um formato que seja reproduzido por um dos drivers de áudio de forma de onda instalados, incluindo o mapeador de ondas.

Para arquivos de som maiores, use os serviços de interface de controle de mídia (MCI). Para obter mais informações, consulte [MCI](mci.md).

 

 