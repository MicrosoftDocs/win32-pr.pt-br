---
description: A função PdhVbGetLogFileSize retorna o tamanho do arquivo de log especificado. Essa função chama PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Função PdhVbGetLogFileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756879"
---
# <a name="pdhvbgetlogfilesize-function"></a>Função PdhVbGetLogFileSize

A função **PdhVbGetLogFileSize** retorna o tamanho do arquivo de log especificado. Essa função chama [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbGetLogFileSize ( \_ ByVal HLog como PDH \_ hLog, \_ ByRef llSize como Long \_ ) como DWORD

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hLog* \[ no\]
</dt> <dd>

Identificador para o arquivo de log. Esse identificador é retornado pela função [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) .

</dd> <dt>

*llSize* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o tamanho do arquivo de log, em bytes.

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



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

