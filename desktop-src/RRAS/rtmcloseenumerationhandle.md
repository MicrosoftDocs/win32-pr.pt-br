---
title: Função RtmCloseEnumerationHandle (RTM. h)
description: O RtmCloseEnumerationHandle encerra uma enumeração especificada e libera os recursos associados.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- Função RtmCloseEnumerationHandle RAS
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009513"
---
# <a name="rtmcloseenumerationhandle-function"></a>Função RtmCloseEnumerationHandle

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

O **RtmCloseEnumerationHandle** encerra uma enumeração especificada e libera os recursos associados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnumerationHandle* \[ no\]
</dt> <dd>

Identificador para a enumeração terminar. Obtenha esse identificador chamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**\_identificador inválido do erro \_**</dt> </dl>       | O parâmetro não é válido.<br/>                                  |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





