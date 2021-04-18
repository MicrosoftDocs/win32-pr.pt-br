---
description: Os aplicativos do Direct3D em tela inteira fornecem um identificador de janela para o tempo de execução do Direct3D.
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: Problemas de multithreading (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d163698e6cc1b4855668d255ed46fd28700d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370103"
---
# <a name="multithreading-issues-direct3d-9"></a>Problemas de multithreading (Direct3D 9)

Os aplicativos do Direct3D em tela inteira fornecem um identificador de janela para o tempo de execução do Direct3D. A janela é conectada pelo tempo de execução. Isso significa que todas as mensagens passadas para o procedimento de mensagem de janela do aplicativo foram examinadas primeiro pelo procedimento de manipulação de mensagens do tempo de execução do Direct3D.

As alterações no modo de exibição são afetadas pelas rotinas de suporte criadas no sistema operacional subjacente. Quando ocorrem alterações no modo, o sistema transmite várias mensagens para todos os aplicativos. Em aplicativos Direct3D, as mensagens são recebidas no thread de procedimento de janela, que não é necessariamente o mesmo thread que chamou [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ou [**IDirect3D9:: CreateDevice**](/windows/desktop/api) (ou a versão final de [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9), que pode causar uma alteração no modo de exibição). O tempo de execução do Direct3D mantém várias seções críticas internamente. Como pelo menos uma dessas seções críticas é mantida pela opção de modo causada por **IDirect3DDevice9:: Reset** ou **IDirect3D9:: CreateDevice**, essas seções críticas ainda são mantidas quando o aplicativo recebe as mensagens de janela relacionadas à alteração de modo.

Esse design tem algumas implicações para aplicativos multissegmentados. Em particular, um aplicativo deve ter a certeza de separar com segurança seus threads de manipulação de mensagens de janela de seus threads do Direct3D. Um aplicativo que causa uma alteração de modo em um thread, mas faz chamadas Direct3D em um thread diferente em seu procedimento de janela está em perigo de deadlock.

Por esses motivos, o Direct3D foi projetado para que os métodos [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), [**IDirect3D9:: CreateDevice**](/windows/desktop/api), [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)ou a versão final de [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) só possam ser chamados do mesmo thread que lida com mensagens de janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
