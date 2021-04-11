---
description: Fornece os métodos necessários para construir e gerenciar uma APDU (unidade de dados do protocolo de aplicativo de cartão inteligente).
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Interface ISCardCmd (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f14291f3777dcdc8b661f96f94d987209100a365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010368"
---
# <a name="iscardcmd-interface"></a>Interface ISCardCmd

\[A interface **ISCardCmd** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **ISCardCmd** fornece os métodos necessários para construir e gerenciar uma APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) de [*cartão inteligente*](../secgloss/s-gly.md) ). Essa interface encapsula dois buffers:

-   O buffer APDU contém a sequência de comandos que será enviada ao cartão.
-   O buffer APDUReply contém dados retornados do cartão após a execução do comando APDU (esses dados também são chamados de APDU de retorno).

O exemplo a seguir mostra um uso típico da interface **ISCardCmd** . A interface **ISCardCmd** é usada para criar um APDU.

**Para enviar uma transação para um cartão específico**

1.  Crie uma interface [**iscard**](iscard.md) e conecte-se a um cartão inteligente.
2.  Crie uma interface **ISCardCmd** .
3.  Crie um comando APDU de cartão inteligente usando a interface [**ISCardISO7816**](iscardiso7816.md) ou um dos métodos de Build **ISCardCmd** .
4.  Execute o comando no cartão inteligente chamando o método de interface [**iscard**](iscard.md) apropriado.
5.  Avalie a resposta retornada.
6.  Repita o procedimento conforme necessário.
7.  Libere a interface **ISCardCmd** e outras, conforme necessário.

## <a name="members"></a>Membros

A interface **ISCardCmd** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardCmd** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **ISCardCmd** tem esses métodos.



| Método                                       | Descrição                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Constrói um APDU de comando válido para transmissão para um cartão inteligente.<br/>                               |
| [**Formatação**](iscardcmd-clear.md)             | Limpa os buffers de mensagens APDU e Reply APDU.<br/>                                             |
| [**Encapsular**](iscardcmd-encapsulate.md) | Encapsula o APDU de comando fornecido em outro APDU de comando para transmissão para um cartão inteligente.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **ISCardCmd** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso           | Descrição                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Leitura/gravação<br/> | Valor atual da ID de classe alternativa.<br/>                                                                                                                        |
| [**APDU**](iscardcmd-get-apdu.md)<br/>                         | Leitura/gravação<br/> | APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) bruto).<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Somente leitura<br/>  | Comprimento do APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Leitura/gravação<br/> | [*Responder APDU*](../secgloss/r-gly.md).<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Leitura/gravação<br/> | Comprimento da APDU de resposta.<br/>                                                                                                                                |
| [**ClassId**](iscardcmd-get-classid.md)<br/>                   | Leitura/gravação<br/> | ID de classe do APDU.<br/>                                                                                                                                    |
| [**Dados**](iscardcmd-get-data.md)<br/>                         | Somente leitura<br/>  | Campo de dados do APDU.<br/>                                                                                                                                  |
| [**Instrução**](iscardcmd-get-instructionid.md)<br/>       | Leitura/gravação<br/> | Byte de ID de instrução do APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Somente leitura<br/>  | Campo Le do APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Leitura/gravação<br/> | Endereço do nó.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Leitura/gravação<br/> | Primeiro byte de parâmetro do APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Leitura/gravação<br/> | Segundo parâmetro byte do APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Somente leitura<br/>  | Terceiro byte de parâmetro do APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Leitura/gravação<br/> | Endereço do nó usado pelo cartão na mensagem de resposta.<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | Leitura/gravação<br/> | [*Responder*](../secgloss/r-gly.md) à palavra de status da mensagem APDU.<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Somente leitura<br/>  | Byte de status de SW1 de mensagem do APDU de resposta.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Somente leitura<br/>  | Responder o byte de status do SW2 da mensagem do APDU.<br/>                                                                                                                    |
| **Tipo**<br/>                                                   | Somente leitura<br/>  | Reservado para uso futuro.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
