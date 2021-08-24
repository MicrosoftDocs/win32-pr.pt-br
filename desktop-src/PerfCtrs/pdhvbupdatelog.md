---
description: A função PdhVbUpdateLog atualiza a consulta atual e grava novos dados no arquivo de log. Essa função chama PdhUpdateLog.
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
ms.openlocfilehash: c7bf8af71d3a0f5cd20a84ef0f1532806e3d3e8d268bd2d322d617534b533cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033606"
---
# <a name="pdhvbupdatelog-function"></a>Função PdhVbUpdateLog

A **função PdhVbUpdateLog** atualiza a consulta atual e grava novos dados no arquivo de log. Essa função chama [**PdhUpdateLog.**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [Funções de Contadores de Desempenho](performance-counters-functions.md).

Função PdhVbUpdateLog( \_ ByVal hLog As PDH \_ HLOG, \_ ByVal szUserString As LPCTSTR \_ )

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hLog* \[ Em\]
</dt> <dd>

Lidar com o arquivo de log a ser atualizado. Esse handle é retornado pela [**função PdhVbOpenLog.**](pdhvbopenlog.md)

</dd> <dt>

*szUserString* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres que especifica os dados a serem adicionados ao arquivo de log. Isso geralmente é usado para comentários dentro do arquivo de log.

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



 

## <a name="remarks"></a>Comentários

Deve haver uma consulta aberta no momento e os contadores desejados devem ser adicionados a ela antes que essa função seja chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

