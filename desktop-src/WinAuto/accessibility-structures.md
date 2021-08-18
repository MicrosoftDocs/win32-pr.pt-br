---
title: Estruturas de acessibilidade
description: Esta seção descreve as estruturas usadas para implementar Windows recursos de acessibilidade. Recursos de acessibilidade do Microsoft Win32.
ms.assetid: 0ff480ae-18e3-413d-b208-a67fbae28c25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576b398769a2cf1dc88d9f7ade8c995988c346e04f1c7becf7aef31cded50e91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994386"
---
# <a name="accessibility-structures"></a>Estruturas de acessibilidade

Esta seção descreve as estruturas usadas para implementar Windows recursos de acessibilidade.

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accesstimeout**](/windows/win32/api/winuser/ns-winuser-accesstimeout)<br/> | Contém informações sobre o período de tempo-máximo associado aos recursos de acessibilidade do Microsoft Win32. <br/> O período de tempo de tempo de acessibilidade é o período de tempo que deve passar sem a entrada do teclado e do mouse antes de o sistema operacional desligar automaticamente os recursos de acessibilidade. O tempo de vida de acessibilidade foi projetado para computadores que são compartilhados por vários usuários para que as opções selecionadas por um usuário não sejam inconvenientes para um usuário subsequente.<br/> Os recursos de acessibilidade afetados pelo tempo-final são os recursos FilterKeys (SlowKeys, BounceKeys e RepeatKeys), MouseKeys, ToggleKeys e StickyKeys. O tempo de vida de acessibilidade também afeta a configuração de modo de alto contraste.<br/> |
| [**FILTERKEYS**](/windows/win32/api/winuser/ns-winuser-filterkeys)<br/>       | Contém informações sobre o recurso de acessibilidade FilterKeys, que permite a um usuário com deficiência definir a taxa de repetição do teclado (RepeatKeys), o atraso de aceitação (SlowKeys) e a taxa de rejeição (BounceKeys). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Highcontrast**](/windows/win32/api/winuser/ns-winuser-highcontrasta)<br/>   | Contém informações sobre o recurso de acessibilidade de alto contraste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Mousekeys**](/windows/win32/api/winuser/ns-winuser-mousekeys)<br/>         | Contém informações sobre o recurso de acessibilidade MouseKeys. Quando o recurso MouseKeys estiver ativo, o usuário poderá usar o teclado numérico para controlar o ponteiro do mouse e clicar, clicar duas vezes, arrastar e soltar. Pressionando NUMLOCK, o usuário pode alternar o teclado numérico entre o modo de controle do mouse e a operação normal. <br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**SERIALKEYS**](/windows/win32/api/winuser/ns-winuser-serialkeysa)<br/>       | Contém informações sobre o recurso de acessibilidade SerialKeys, que interpreta dados de um auxílio de comunicação anexado a uma porta serial como comandos que estão fazendo com que o sistema simule a entrada do teclado e do mouse. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Soundsentry**](/windows/win32/api/winuser/ns-winuser-soundsentrya)<br/>     | Contém informações sobre o recurso de acessibilidade SoundSentry. Quando o recurso SoundSentry está em, o computador exibe uma indicação visual somente quando um som é gerado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Stickykeys**](/windows/win32/api/winuser/ns-winuser-stickykeys)<br/>       | Contém informações sobre o recurso de acessibilidade StickyKeys. Quando o recurso StickyKeys está em, o usuário pode pressionar uma tecla modificadora (SHIFT, CTRL ou ALT) e, em seguida, outra tecla na sequência, em vez de ao mesmo tempo, para inserir caracteres deslocados (modificados) e outras combinações de teclas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Togglekeys**](/windows/win32/api/winuser/ns-winuser-togglekeys)<br/>       | Contém informações sobre o recurso de acessibilidade ToggleKeys. Quando o recurso ToggleKeys está on, o computador emite um tom de tom alto sempre que o usuário liga a tecla CAPS LOCK, NUM LOCK ou SCROLL LOCK e um tom baixo sempre que o usuário desliga uma dessas chaves. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Recursos de acessibilidade](../accessibility/accessibility.md)
</dt> </dl>

 

