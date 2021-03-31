---
description: A interface ISCardISO7816 fornece métodos para implementar a funcionalidade ISO 7816-4.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: Interface ISCardISO7816 (Scardssp. h)
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
ms.openlocfilehash: 09e5dc9e84a36148e240e4ba2d31f04216454994
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662136"
---
# <a name="iscardiso7816-interface"></a>Interface ISCardISO7816

\[A interface **ISCardISO7816** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **ISCardISO7816** fornece métodos para implementar a funcionalidade ISO 7816-4. Com exceção de [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md), esses métodos criam um comando de APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que é encapsulado em um objeto [**ISCardCmd**](iscardcmd.md) .

A especificação ISO 7816-4 define os comandos padrão disponíveis em [*cartões inteligentes*](../secgloss/s-gly.md). A especificação também define como um comando APDU de cartão inteligente deve ser construído e enviado ao cartão inteligente para execução. Essa interface automatiza o processo de criação.

O exemplo a seguir mostra um uso típico da interface **ISCardISO7816** . Nesse caso, a interface **ISCardISO7816** é usada para criar um comando APDU.

**Para enviar uma transação para um cartão específico**

1.  Crie uma interface **ISCardISO7816** e [**ISCardCmd**](iscardcmd.md) .

    A interface [**ISCardCmd**](iscardcmd.md) é usada para encapsular o APDU.

2.  Chame o método apropriado da interface **ISCardISO7816** , passando os parâmetros necessários e o ponteiro de interface [**ISCardCmd**](iscardcmd.md) .

    O comando ISO 7816-4 APDU será compilado e encapsulado na interface [**ISCardCmd**](iscardcmd.md) .

3.  Libere as interfaces **ISCardISO7816** e [**ISCardCmd**](iscardcmd.md) .

> [!Note]  
> Nas páginas de referência do método, se uma sequência de bits em uma tabela não for definida, suponha que a sequência de bits seja reservada para uso futuro ou proprietária para um fornecedor específico.

 

## <a name="members"></a>Membros

A interface **ISCardISO7816** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardISO7816** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardISO7816** tem esses métodos.



| Método                                                             | Descrição                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | Constrói um comando que acrescenta um registro ao final de um arquivo elementar (EF).<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | Define parte do conteúdo de um EF para seu estado de apagamento lógico, em sequência, a partir de um determinado deslocamento.<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | Atualiza condicionalmente o status de segurança usando o resultado da Computação pelo cartão, com base em um desafio emitido anteriormente pelo cartão (por exemplo, pelo \_ comando ins get \_ Challenge), uma chave secreta possivelmente armazenada no cartão e dados de autenticação transmitidos pelo dispositivo de interface.<br/> |
| [**Getchallenge**](iscardiso7816-getchallenge.md)                 | Requer a emissão de um desafio para uso em um procedimento relacionado à segurança.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Recupera um único objeto de dados primitivos ou um conjunto de objetos de dados contidos em um objeto de dados construído, com base no tipo de arquivo especificado.<br/>                                                                                                                                                          |
| [**GetResponse**](iscardiso7816-getresponse.md)                   | Transmite do cartão para o dispositivo de interface APDUs que, caso contrário, não pôde ser transmitido pelos protocolos disponíveis.<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | Inicia a computação dos dados de autenticação pelo cartão usando os dados de desafio enviados do dispositivo de interface e um segredo relevante armazenado no cartão.<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | Abre e fecha os canais lógicos.<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | Armazena um objeto de dados primitivos ou um ou mais objetos de dados contidos em um objeto de dados construído, dentro do contexto atual do [*Resource Manager*](../secgloss/r-gly.md).<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | Constrói um comando que adquire uma mensagem de resposta que fornece a parte do conteúdo de um EF com estrutura transparente.<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | Constrói um comando que lê o conteúdo dos registros especificados de um arquivo elementar.<br/>                                                                                                                                                                                                            |
| [**Selecionarfile**](iscardiso7816-selectfile.md)                     | Define um arquivo atual em um canal lógico.<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | Atribui um byte de ID de classe padrão que será usado em todas as operações durante a construção de um comando ISO 7816-4 APDU.<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | Inicia a atualização dos bits já presentes em um EF com os bits fornecidos no comando APDU.<br/>                                                                                                                                                                                                      |
| [**Atualizarregistro**](iscardiso7816-updaterecord.md)                 | Constrói um comando que inicia a atualização de um registro específico.<br/>                                                                                                                                                                                                                                  |
| [**Verificar**](iscardiso7816-verify.md)                             | Inicia a comparação no cartão dos dados de verificação enviados do dispositivo de interface com os dados de referência armazenados no cartão.<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | Inicia a gravação de valores binários em um EF.<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | Constrói um comando que grava um registro.<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



 

 
