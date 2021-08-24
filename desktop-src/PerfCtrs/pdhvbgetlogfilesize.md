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
ms.openlocfilehash: cd3925eee621ac205615f17b26767096151d459628ca7d331a7aaee3336b27ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674786"
---
# <a name="pdhvbgetlogfilesize-function"></a>Função PdhVbGetLogFileSize

A **função PdhVbGetLogFileSize** retorna o tamanho do arquivo de log especificado. Essa função chama [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [Funções de Contadores de Desempenho](performance-counters-functions.md).

Função PdhVbGetLogFileSize( \_ ByVal hLog As PDH \_ HLOG, \_ ByRef llSize As LONG \_ ) as DWORD

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hLog* \[ Em\]
</dt> <dd>

Lidar com o arquivo de log. Esse handle é retornado pela [**função PdhOpenLog.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)

</dd> <dt>

*llSize* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o tamanho do arquivo de log, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará 0.

Se a função falhar, o valor de retorno será um código [de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de erro [PDH](pdh-error-codes.md). A seguir estão os valores possíveis.



| Código de retorno                                                                                                | Descrição                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER INSUFICIENTE DE PDH \_ \_**</dt> </dl>   | Os dados solicitados são maiores do que o buffer fornecido. Não é possível retornar os dados solicitados.<br/> |
| <dl> <dt>**ARGUMENTO INVÁLIDO \_ PDH \_**</dt> </dl>      | Um ou mais buffers de cadeia de caracteres não tem o tamanho correto.<br/>                                  |
| <dl> <dt>**PDH \_ INVALID \_ HANDLE**</dt> </dl>        | O identificador não é um objeto PDH válido.<br/>                                                       |
| <dl> <dt>**ERRO DE ABERTURA DO \_ \_ ARQUIVO \_ DE LOG PDH \_**</dt> </dl> | Não é possível abrir o arquivo de log especificado.<br/>                                                      |
| <dl> <dt>**ARQUIVO PDH \_ \_ NÃO \_ ENCONTRADO**</dt> </dl>       | Não é possível encontrar o arquivo especificado.<br/>                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

