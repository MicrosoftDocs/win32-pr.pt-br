---
description: Permite abrir e gerenciar uma conexão com um cartão inteligente.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interface iscard (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502355"
---
# <a name="iscard-interface"></a>Interface iscard

\[A interface **iscard** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **iscard** permite que você abra e gerencie uma conexão a um [*cartão inteligente*](../secgloss/s-gly.md). Cada conexão com um cartão requer uma única instância correspondente da interface **iscard** .

O Gerenciador de [*recursos*](../secgloss/r-gly.md) de cartão inteligente deve estar disponível sempre que uma instância do **iscard** for criada. Se esse serviço não estiver disponível, a criação da interface falhará.

O exemplo a seguir mostra um uso típico da interface **iscard** . A interface **iscard** é usada para se conectar ao cartão inteligente, enviar uma [*transação*](../secgloss/t-gly.md)e liberar o cartão inteligente.

**Para enviar uma transação para um cartão específico**

1.  Crie uma interface **iscard** .
2.  Anexe a um cartão inteligente especificando um [*leitor*](../secgloss/r-gly.md) de cartão inteligente ou usando um identificador válido estabelecido anteriormente.
3.  Crie comandos de transação com as interfaces de cartão inteligente [**ISCardCmd**](iscardcmd.md)e [**ISCardISO7816**](iscardiso7816.md) .
4.  Use **iscard** para enviar os comandos de transação para processamento pelo cartão inteligente.
5.  Use **iscard** para liberar o cartão inteligente.
6.  Libere a interface **iscard** .

## <a name="members"></a>Membros

A interface **Iscard** é herdada da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Iscard** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **iscard** tem esses métodos.



| Método                                          | Descrição                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Anexa um objeto a um identificador de cartão inteligente aberto e configurado.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Abre o cartão inteligente no leitor nomeado.<br/>                                                                                                                                                                            |
| [**Detach**](iscard-detach.md)                 | Fecha a conexão aberta com o cartão inteligente.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Alega acesso exclusivo ao cartão inteligente.<br/>                                                                                                                                                                           |
| [**Anexar novamente**](iscard-reattach.md)             | Redefine e reinicializa o cartão inteligente.<br/>                                                                                                                                                                             |
| [**Transação**](iscard-transaction.md)       | Executa uma operação de gravação e leitura no objeto de comando de cartão inteligente ([*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md)).<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Libera o acesso exclusivo ao cartão inteligente.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Propriedades

A interface **iscard** tem essas propriedades.



| Propriedade                                               | Tipo de acesso          | Descrição                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Somente leitura<br/> | Recupera a [*cadeia de caracteres ATR*](../secgloss/a-gly.md) do cartão inteligente.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Somente leitura<br/> | Recupera o identificador do cartão inteligente conectado.<br/>                                                                                                                                  |
| [**Contexto**](iscard-get-context.md)<br/>       | Somente leitura<br/> | Recupera o identificador de contexto atual do [*Resource Manager*](../secgloss/r-gly.md) .<br/>                            |
| [**Protocolo**](iscard-get-protocol.md)<br/>     | Somente leitura<br/> | Recupera o identificador do protocolo atualmente em uso no cartão inteligente.<br/>                                                                                                        |
| [**Status**](iscard-get-status.md)<br/>         | Somente leitura<br/> | Recupera o [*estado*](../secgloss/s-gly.md) atual em que o [*cartão inteligente*](../secgloss/s-gly.md) está.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | \_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 
