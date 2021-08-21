---
title: Método Listen
description: Método Listen
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc87a57d1ebdd3f36a2d56d85e0754f5005fd6c356fc9af98760bd0db90605f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748650"
---
# <a name="listen-method"></a>Método Listen

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ativa o modo de escuta (reconhecimento de fala) por um período de tempo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters***("**_CharacterID_*_"). Estado de_ *  *Escuta*



| Parte    | Descrição                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Obrigatórios. Um valor booliana que determina se o modo de escuta deve ser ativar ou desativar. **True** Ativa o modo de escuta. <br/> **False** Desliga o modo de escuta.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Definir esse método como **True** habilita o modo de escuta (ativa o reconhecimento de fala) por um período fixo (10 segundos). Embora não seja possível definir o valor do tempo-expirado, você pode desativar o modo de escuta antes que o tempo-expirar. Se você (ou outro cliente) definir com êxito o modo de Escuta e tentar definir essa propriedade como **True** antes que o tempo-expirar, o método terá êxito e redefinirá o tempo-expirado. No entanto, se o modo de Escuta estiver em porque o usuário está pressionando a tecla Listening, o método será bem-sucedido, mas o tempo-tempo será ignorado e o modo de escuta terminará com base na interação do usuário com a tecla Listening.

Esse método só terá êxito quando chamado pelo cliente ativo de entrada e se os serviços de fala foram iniciados. Para garantir que os serviços de fala tenham sido iniciados, consulte ou de definido [**o SRModeID**](srmodeid-property.md) ou de definir [**a**](/windows/desktop/lwef/the-command-object) configuração Voz para um Comando antes de chamar **Escutar** caso contrário, o método falhará. [](voice-property.md) Para detectar o sucesso desse método, chame-o como uma função e ele retornará um valor booliana que indica se o método foi bem-sucedido.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



O método também falhará se o usuário estiver pressionando a tecla Listening e você tentar definir **Escutar** como **False.** No entanto, se o usuário tiver liberado a tecla Listening e o modo de escuta não tiver tempo de vida, ele terá êxito.

**A** escuta também falhará se não houver nenhum mecanismo de fala compatível disponível que corresponde à configuração [**LanguageID**](languageid-property.md) do caractere, se o usuário tiver desabilitado a entrada de fala usando a folha de propriedades do Microsoft Agent ou se o dispositivo de áudio estiver ocupado.

Quando você definiu esse método com êxito como **True,** o servidor dispara o [**evento ListenStart.**](listenstart-event.md) O servidor envia [**ListenComplete quando**](listencomplete-event.md) o tempo-final do modo de escuta for concluído ou quando você definir **Escutar** como **False.**

Esse método não chama parar e [**reproduzir**](stop-method.md) automaticamente uma animação de estado de Escuta como o servidor faz quando a tecla Listening é pressionada. Isso permite que você determine se a animação atual deve ser interrompida usando a animação [**ListenStart**](listenstart-event.md) chamando **Parar** e tocando sua própria animação apropriada. No entanto, o servidor chama **Parar** e reproduz uma animação de estado auditivo quando um enunciado do usuário é detectado.

## <a name="see-also"></a>Consulte Também

[**Propriedade LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)


 

