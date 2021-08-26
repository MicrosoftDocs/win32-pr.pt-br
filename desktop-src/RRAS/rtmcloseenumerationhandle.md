---
title: Função RtmCloseEnumerationHandle (Rtm.h)
description: O RtmCloseEnumerationHandle encerra uma enumeração especificada e libera os recursos associados.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- Função RAS RtmCloseEnumerationHandle
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
ms.openlocfilehash: 0313cc594b0629509ffcee65ea333caa9dbc373de323dc656a6028bc26e14317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081046"
---
# <a name="rtmcloseenumerationhandle-function"></a>Função RtmCloseEnumerationHandle

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

O **RtmCloseEnumerationHandle** encerra uma enumeração especificada e libera os recursos associados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnumerationHandle* \[ Em\]
</dt> <dd>

Lidar com a enumeração a ser encerrada. Obtenha esse handle chamando [**RtmCreateEnumerationHandle.**](rtmcreateenumerationhandle.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NENHUM \_ ERRO.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ INVALID \_ HANDLE**</dt> </dl>       | O parâmetro não é válido.<br/>                                  |
| <dl> <dt>**ERRO \_ NENHUM RECURSO DO \_ \_ SISTEMA**</dt> </dl> | Não há recursos suficientes para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





