---
description: A função PdhVbAddCounter cria uma entrada de contador no objeto de consulta especificado e retorna um identificador para esse contador após a conclusão bem-sucedida.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Função PdhVbAddCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754614"
---
# <a name="pdhvbaddcounter-function"></a>Função PdhVbAddCounter

A função **PdhVbAddCounter** cria uma entrada de contador no objeto de consulta especificado e retorna um identificador para esse contador após a conclusão bem-sucedida.

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbAddCounter ( \_ ByVal QueryHandle as Long, \_ ByVal Compath como String, \_ ByVal lide como Long \_ ) enquanto longo

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

ID da consulta à qual este contador deve ser atribuído. Esse valor é retornado pela função [**PdhVbOpenQuery**](pdhvbopenquery.md) .

</dd> <dt>

*CounterPath* 
</dt> <dd>

Cadeia de texto que especifica o nome do caminho do contador a ser adicionado à consulta. O conteúdo dessa cadeia de caracteres deve ser um caminho de contador válido, conforme obtido no navegador do contador ou outra fonte.

</dd> <dt>

*Manipulador* 
</dt> <dd>

Referência exclusiva que identifica esse contador na consulta. Essa variável deve ser inicializada para zero antes de a função ser chamada. Ele contém um valor válido em retornar somente se a função for concluída com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará um inteiro **longo** igual a erro de \_ êxito e um novo identificador na variável de *manipulador* .

Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md). Os valores a seguir são possíveis.



| Código de retorno                                                                                                     | Descrição                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_argumento inválido de PDH \_**</dt> </dl>           | Um ou mais argumentos são inválidos ou incorretos.<br/>              |
| <dl> <dt>**\_falha de \_ alocação de memória de PDH \_**</dt> </dl> | Não foi possível alocar um buffer de memória.<br/>                            |
| <dl> <dt>**\_identificador inválido de PDH \_**</dt> </dl>             | O identificador de consulta não é válido.<br/>                                     |
| <dl> <dt>**\_CSTATUS PDH \_ sem \_ contador**</dt> </dl>        | O contador especificado não foi encontrado.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ nenhum \_ objeto**</dt> </dl>         | O objeto especificado não pôde ser encontrado.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ nenhum \_ computador**</dt> </dl>        | Não foi possível criar uma entrada de computador.<br/>                             |
| <dl> <dt>**CSTATUS de PDH \_ \_ inválido \_ COUNTERNAME**</dt> </dl>   | Uma cadeia de caracteres de caminho de nome de contador vazio foi passada.<br/>                   |
| <dl> <dt>**\_função PDH \_ não \_ encontrada**</dt> </dl>        | Não foi possível determinar a função de cálculo deste contador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

