---
title: Tratamento de erros (Windows Media Player SDK)
description: Tratamento de erros
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, tratamento de erro
- Windows Media Player de objeto, tratamento de erro
- modelo de objeto, tratamento de erro
- Windows Media Player ActiveX controle, tratamento de erro
- ActiveX controle, tratamento de erros
- Windows Media Player Controle ActiveX dispositivo móvel, tratamento de erros
- Windows Media Player Dispositivo móvel, tratamento de erros
- guia de migração, tratamento de erros
- tratamento de erro no modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378d5f41b9b2c664345ee9c94964545c8ff9504c98c4e29244818a28ff398ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935103"
---
# <a name="error-handling-windows-media-player-sdk"></a>Tratamento de erros (Windows Media Player SDK)

O Windows Media Player controle ActiveX 6.4 fornece tratamento de erro padrão exibindo mensagens de erro nas caixas de diálogo e na barra de status. Você também pode fornecer tratamento de erro personalizado processando erros em seu script. O tratamento de erros é orientado a eventos, o que significa que você recebe uma notificação para cada erro e deve decidir como lidar com cada evento de erro quando ele ocorre. Para obter mais informações sobre como lidar com erros usando o modelo de objeto versão 6.4, consulte a seção Tratamento de erros do Guia do Modelo de Objeto do Player versão 6.4, que faz parte do SDK do Windows Media Player.

O Windows Media Player modelo de objeto 7 ou posterior fornece o **objeto Error** e o **objeto ErrorItem** para tratar erros. Esses dois objetos funcionam em conjunto para fornecer um mecanismo de tratamento de erros que fornece controle completo e flexível do processo de tratamento de erros. O **objeto Error** fornece acesso a uma coleção de objetos **ErrorItem;** cada **objeto ErrorItem** fornece detalhes sobre uma mensagem de erro individual.

Quando ocorre um erro, as informações de erro são postadas em uma fila de erros. A fila é uma coleção de **objetos ErrorItem.** À medida que cada erro é adicionado à fila, ele é associado a um número de índice (começando com zero) que pode ser usado para identificar o objeto **ErrorItem** específico. O *Erro*. **A propriedade errorCount** recupera o número de erros na fila de erros. Como os números de índice são baseados em zero, o erro mais recente postado na fila sempre terá um valor de índice igual ao *Erro*. **errorCount** menos um.

Você pode criar um manipulador de eventos de erro para Windows Media Player usando script. O exemplo JScript a seguir mostra como recuperar o item de erro mais recente da fila de erros e exibir o código de erro e a descrição do erro usando o modelo de objeto Windows Media Player 7 ou posterior. O **objeto** Player foi criado com ID = "WMP9".


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



O **objeto Error** tem dois métodos adicionais que você pode usar. O *Erro*. **O método clearErrorQueue** permite remover todos os erros da fila de erros e redefinir o número do índice para zero. Você tem controle total sobre esse processo; você pode manter os erros na fila enquanto precisar que eles sejam disponibilizados e, em seguida, esvazie a fila quando terminar de tratar os erros.

O *Erro*. **O método webHelp** fornece uma maneira de exibir as informações de erro mais atuais para o usuário usando a Internet. Quando chamado, esse método transfere todas as informações relevantes sobre o primeiro erro na fila (aquele com índice zero) para a Ajuda da Web do Microsoft Windows Media Player, que exibe mais informações sobre o erro na janela atual do navegador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto Error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Guia de migração de modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




