---
title: Método de escuta
description: Método de escuta
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007419"
---
# <a name="listen-method"></a>Método de escuta

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ativa o modo de escuta (reconhecimento de fala) por um período de tempo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do. ***Caracteres * * * * ("*** characterid * * *").* *  *Estado* de escuta



| Parte    | Descrição                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Obrigatórios. Um valor booliano que determina se o modo de escuta deve ser ativado ou desativado. **Verdadeiro** Ativa o modo de escuta. <br/> **Falso** Desativa o modo de escuta.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Definir esse método como **true** habilita o modo de escuta (ativa o reconhecimento de fala) por um período de tempo fixo (10 segundos). Embora não seja possível definir o valor do tempo limite, você pode desligar o modo de escuta antes que o tempo limite expire. Se você (ou outro cliente) tiver definido o modo de escuta com êxito e tentar definir essa propriedade como **true** antes da expiração do tempo limite, o método terá êxito e redefinirá o tempo limite. No entanto, se o modo de escuta estiver ativado porque o usuário está pressionando a tecla de escuta, o método terá sucesso, mas o tempo limite será ignorado e o modo de escuta terminará com base na interação do usuário com a chave de escuta.

Esse método tem sucesso apenas quando chamado pelo cliente de entrada-ativo e se os serviços de fala foram iniciados. Para garantir que os serviços de fala tenham sido iniciados, consulte ou defina o [**SRModeID**](srmodeid-property.md) ou defina a configuração de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) antes de chamar **Listen** , caso contrário, o método falhará. Para detectar o sucesso desse método, chame-o como uma função e ele retornará um valor booliano indicando se o método teve êxito.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



O método também falhará se o usuário estiver pressionando a tecla de escuta e você tentar definir **escutar** como **false**. No entanto, se o usuário tiver liberado a chave de escuta e o modo de escuta não tiver expirado, ele terá sucesso.

A **escuta** também falhará se não houver nenhum mecanismo de fala compatível disponível que corresponda à configuração [**LanguageID**](languageid-property.md) do caractere, o usuário desabilitou a entrada de fala usando a folha de propriedades do Microsoft Agent ou o dispositivo de áudio está ocupado.

Quando você define com êxito esse método como **true**, o servidor dispara o evento [**ListenStart**](listenstart-event.md) . O servidor envia [**ListenComplete**](listencomplete-event.md) quando o tempo limite do modo de escuta é concluído ou quando você define **Listen** como **false**.

Esse método não chama automaticamente [**Stop**](stop-method.md) e executa uma animação de estado de escuta conforme o servidor faz quando a tecla de escuta é pressionada. Isso permite que você determine se deve interromper a animação atual usando a animação [**ListenStart**](listenstart-event.md) chamando **Stop** e jogando sua própria animação apropriada. No entanto, o servidor chama **Stop** e executa uma animação de estado audição quando um usuário expressão é detectado.

## <a name="see-also"></a>Consulte Também

[**Propriedade LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)


 

