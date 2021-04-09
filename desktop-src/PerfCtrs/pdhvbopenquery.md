---
description: A função PdhVbOpenQuery cria e Inicializa uma estrutura de consulta exclusiva que é usada para gerenciar a coleta de dados de desempenho.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Função PdhVbOpenQuery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091635"
---
# <a name="pdhvbopenquery-function"></a>Função PdhVbOpenQuery

A função **PdhVbOpenQuery** cria e Inicializa uma estrutura de consulta exclusiva que é usada para gerenciar a coleta de dados de desempenho.

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbOpenQuery ( \_ ByVal QueryHandle as Long \_ ) enquanto longo

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variável que é limpa (igual a 0) antes que a função seja chamada e, se a função for bem-sucedida, conterá a ID exclusiva da consulta criada e aberta. Esse identificador é usado nas chamadas subsequentes para outras funções de PDH para identificar a consulta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará um inteiro **longo** igual a erro de \_ êxito e um novo identificador na variável *QueryHandle* .

Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md). Os valores a seguir são possíveis.



| Código de retorno                                                                                                     | Descrição                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**\_argumento inválido de PDH \_**</dt> </dl>           | O argumento é inválido ou está incorreto.<br/>             |
| <dl> <dt>**\_falha de \_ alocação de memória de PDH \_**</dt> </dl> | Não foi possível alocar um buffer de memória temporário.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

