---
title: Out-Only parâmetros de ponteiro exclusivos ou completos não aceitos
description: Ponteiros únicos ou completos que são \ out somente não são aceitos pelo compilador MIDL. Essas especificações fazem com que o compilador MIDL gere uma mensagem de erro.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9511c21045892eb7a5b3230d8f0180578b489b06b5b5402fb0b11f6a3ff31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927565"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only parâmetros de ponteiro exclusivos ou completos não aceitos

Ponteiros exclusivos ou completos que estão \[ [fora](/windows/desktop/Midl/out-idl) \] de somente não são aceitos pelo compilador MIDL. Essas especificações fazem com que o compilador MIDL gere uma mensagem de erro.

O stub de servidor gerado automaticamente precisa alocar memória para o ponteiro Referent para que o aplicativo de servidor possa armazenar dados nessa área de memória. De acordo com a definição de um parâmetro somente **\[ out \]**, nenhuma informação sobre o parâmetro é transmitida do cliente para o servidor. No caso de um ponteiro exclusivo, que pode usar o valor NULL, o stub do servidor não tem informações suficientes para duplicar corretamente o ponteiro exclusivo no espaço de endereço do servidor, nem o stub tem informações sobre se o ponteiro deve apontar para um endereço válido ou se deve ser definido como nulo. Portanto, essa combinação não é permitida.

Em vez de \[ **out**, [Unique](/windows/desktop/Midl/unique) \] ou \[ **out**, ponteiros [PTR](/windows/desktop/Midl/ptr) \] , use \[ ponteiros **in**, **out**, **Unique** \] ou \[ **in**, **out**, **PTR** \] ou use outro nível de indireção, como um ponteiro de referência que aponte para o ponteiro exclusivo ou completo válido.

 

 