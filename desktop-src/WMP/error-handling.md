---
title: Tratamento de erro (SDK do Windows Media Player)
description: Tratamento de erros
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, tratamento de erros
- Modelo de objeto do Windows Media Player, tratamento de erros
- modelo de objeto, tratamento de erro
- Controle ActiveX do Windows Media Player, tratamento de erros
- Controle ActiveX, tratamento de erros
- Controle ActiveX móvel do Windows Media Player, tratamento de erros
- Windows Media Player Mobile, tratamento de erros
- Guia de migração, tratamento de erros
- tratamento de erro no modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085036"
---
# <a name="error-handling-windows-media-player-sdk"></a>Tratamento de erro (SDK do Windows Media Player)

O controle ActiveX do Windows Media Player 6,4 Fornece tratamento de erros padrão exibindo mensagens de erro em caixas de diálogo e na barra de status. Você também pode fornecer tratamento de erros personalizado processando erros em seu script. O tratamento de erros é controlado por eventos, o que significa que você recebe uma notificação para cada erro e deve decidir como lidar com cada evento de erro quando ele ocorre. Para obter mais informações sobre como tratar erros usando o modelo de objeto da versão 6,4, consulte a seção tratamento de erros do guia do modelo de objeto da versão 6,4 do Player, que faz parte do SDK do Windows Media Player.

O modelo de objeto do Windows Media Player 7 ou posterior fornece o objeto **Error** e o objeto **ErrorItem** para lidar com erros. Esses dois objetos funcionam em conjunto para fornecer a você um mecanismo de tratamento de erros que oferece controle completo e flexível do processo de tratamento de erros. O objeto **Error** fornece acesso a uma coleção de objetos **ErrorItem** ; cada objeto **ErrorItem** fornece detalhes sobre uma mensagem de erro individual.

Quando ocorre um erro, as informações de erro são postadas em uma fila de erros. A fila é uma coleção de objetos **ErrorItem** . À medida que cada erro é adicionado à fila, ele é associado a um número de índice (começando com zero) que pode ser usado para identificar o objeto **ErrorItem** específico. O *erro*. a propriedade **errorCount** recupera o número de erros na fila de erros. Como os números de índice são baseados em zero, o erro mais recente Postado na fila sempre terá um valor de índice igual a *erro*. **errorCount** menos um.

Você pode criar um manipulador de eventos de erro para o Windows Media Player usando o script. O exemplo de JScript a seguir mostra como recuperar o item de erro mais recente da fila de erros e exibir o código de erro e a descrição do erro usando o modelo de objeto do Windows Media Player 7 ou posterior. O objeto de **jogador** foi criado com ID = "WMP9".


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



O objeto de **erro** tem dois métodos adicionais que você pode usar. O *erro*. o método **clearErrorQueue** permite remover todos os erros da fila de erros e redefinir o número de índice para zero. Você tem controle total sobre esse processo; Você pode manter os erros na fila pelo tempo que precisar que estejam disponíveis e, em seguida, esvaziar a fila quando terminar de lidar com os erros.

O *erro*. o método **WebHelp** fornece uma maneira de exibir as informações de erro mais recentes para o usuário usando a Internet. Quando chamado, esse método transfere todas as informações relevantes sobre o primeiro erro na fila (aquela com índice zero) para a ajuda da Web do Microsoft Windows Media Player, que exibe informações adicionais sobre o erro na janela atual do navegador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto Error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




