---
description: A função de função PdhVbUpdateLog atualiza a consulta atual e grava novos dados no arquivo de log. Essa função chama PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Função PdhVbUpdateLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758288"
---
# <a name="pdhvbupdatelog-function"></a>Função PdhVbUpdateLog

A função de função **PdhVbUpdateLog** atualiza a consulta atual e grava novos dados no arquivo de log. Essa função chama [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbUpdateLog ( \_ ByVal HLog as \_ hLog PDH, \_ ByVal szUserString as LPCTSTR \_ )

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hLog* \[ no\]
</dt> <dd>

Identificador para o arquivo de log a ser atualizado. Esse identificador é retornado pela função [**PdhVbOpenLog**](pdhvbopenlog.md) .

</dd> <dt>

*szUserString* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres que especifica os dados a serem adicionados ao arquivo de log. Isso geralmente é usado para comentários no arquivo de log.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará 0.

Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md). Os valores a seguir são possíveis.



| Código de retorno                                                                                                | Descrição                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_buffer insuficiente de PDH \_**</dt> </dl>   | Os dados solicitados são maiores que o buffer fornecido. Não é possível retornar os dados solicitados.<br/> |
| <dl> <dt>**\_argumento inválido de PDH \_**</dt> </dl>      | Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.<br/>                                  |
| <dl> <dt>**\_identificador inválido de PDH \_**</dt> </dl>        | O identificador não é um objeto PDH válido.<br/>                                                       |
| <dl> <dt>**\_ \_ \_ erro ao abrir arquivo de log PDH \_**</dt> </dl> | Não é possível abrir o arquivo de log especificado.<br/>                                                      |
| <dl> <dt>**\_arquivo PDH \_ não \_ encontrado**</dt> </dl>       | Não é possível localizar o arquivo especificado.<br/>                                                          |



 

## <a name="remarks"></a>Comentários

Deve haver uma consulta aberta no momento e os contadores desejados devem ser adicionados a ela antes que essa função seja chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

