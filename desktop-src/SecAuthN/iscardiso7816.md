---
description: A interface ISCardISO7816 fornece métodos para implementar a funcionalidade ISO 7816-4.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: Interface ISCardISO7816 (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aeda73e926ca9276e7e41ecfe966a088e311f4077040abe9eadb4ffc1701bfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014336"
---
# <a name="iscardiso7816-interface"></a>Interface ISCardISO7816

\[A interface **ISCardISO7816** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **ISCardISO7816** fornece métodos para implementar a funcionalidade ISO 7816-4. Com exceção de [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md), esses métodos criam um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados de protocolo de aplicativo) encapsulado em [**um objeto ISCardCmd.**](iscardcmd.md)

A especificação ISO 7816-4 define comandos padrão disponíveis em [*cartões inteligentes.*](../secgloss/s-gly.md) A especificação também define como um comando APDU de cartão inteligente deve ser construído e enviado ao cartão inteligente para execução. Essa interface automatiza o processo de criação.

O exemplo a seguir mostra um uso típico da interface **ISCardISO7816.** Nesse caso, a interface **ISCardISO7816** é usada para criar um comando APDU.

**Para enviar uma transação para um cartão específico**

1.  Crie uma **interface ISCardISO7816** [**e ISCardCmd.**](iscardcmd.md)

    A interface [**ISCardCmd**](iscardcmd.md) é usada para encapsular o APDU.

2.  Chame o método apropriado da interface **ISCardISO7816,** passando os parâmetros necessários e o ponteiro da interface [**ISCardCmd.**](iscardcmd.md)

    O comando APDU ISO 7816-4 será criado e encapsulado na interface [**ISCardCmd.**](iscardcmd.md)

3.  Libere as **interfaces ISCardISO7816** [**e ISCardCmd.**](iscardcmd.md)

> [!Note]  
> Nas páginas de referência do método, se uma sequência de bits em uma tabela não estiver definida, suponha que essa sequência de bits seja reservada para uso futuro ou proprietária para um fornecedor específico.

 

## <a name="members"></a>Membros

A interface **ISCardISO7816** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardISO7816** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardISO7816** tem esses métodos.



| Método                                                             | Descrição                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | Constrói um comando que acrescenta um registro ao final de um EF (arquivo elementar).<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | Define parte do conteúdo de um EF para seu estado lógico apagado, sequencialmente, começando de um deslocamento determinado.<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | Atualiza condicionalmente o status de segurança usando o resultado da computação pelo cartão, com base em um desafio emitido anteriormente pelo cartão (por exemplo, pelo comando GET CHALLENGE do INS), uma chave secreta possivelmente armazenada no cartão e os dados de autenticação transmitidos pelo dispositivo \_ \_ de interface.<br/> |
| [**GetChallenge**](iscardiso7816-getchallenge.md)                 | Requer a emissão de um desafio para uso em um procedimento relacionado à segurança.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Recupera um único objeto de dados primitivo ou um conjunto de objetos de dados contidos em um objeto de dados construído, com base no tipo de arquivo especificado.<br/>                                                                                                                                                          |
| [**Getresponse**](iscardiso7816-getresponse.md)                   | Transmite do cartão para as APDUs do dispositivo de interface que, de outra forma, não puderam ser transmitidas pelos protocolos disponíveis.<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | Inicia o cálculo dos dados de autenticação pelo cartão usando os dados de desafio enviados do dispositivo de interface e um segredo relevante armazenado no cartão.<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | Abre e fecha canais lógicos.<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | Armazena um objeto de dados primitivo ou um ou mais objetos de dados contidos em um objeto de dados construído, dentro do contexto [*atual do resource manager*](../secgloss/r-gly.md).<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | Constrói um comando que adquire uma mensagem de resposta que fornece essa parte do conteúdo de um EF com estrutura transparente.<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | Constrói um comando que lê o conteúdo dos registros especificados de um arquivo elementar.<br/>                                                                                                                                                                                                            |
| [**SelectFile**](iscardiso7816-selectfile.md)                     | Define um arquivo atual dentro de um canal lógico.<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | Atribui um byte de ID de classe padrão que será usado em todas as operações ao construir um APDU de comando ISO 7816-4.<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | Inicia a atualização dos bits já presentes em um EF com os bits dados no comando APDU.<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | Constrói um comando que inicia a atualização de um registro específico.<br/>                                                                                                                                                                                                                                  |
| [**Verificar**](iscardiso7816-verify.md)                             | Inicia a comparação no cartão dos dados de verificação enviados do dispositivo de interface com os dados de referência armazenados no cartão.<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | Inicia a escrita de valores binários em um EF.<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | Constrói um comando que grava um registro.<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



 

 
