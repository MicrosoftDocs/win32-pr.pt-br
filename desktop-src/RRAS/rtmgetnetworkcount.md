---
title: Função RtmGetNetworkCount (RTM. h)
description: A função RtmGetNetworkCount recupera o número de redes para as quais o Gerenciador de tabela de roteamento tem rotas.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- Função RtmGetNetworkCount RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644627"
---
# <a name="rtmgetnetworkcount-function"></a>Função RtmGetNetworkCount

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmGetNetworkCount** recupera o número de redes para as quais o Gerenciador de tabela de roteamento tem rotas.

## <a name="syntax"></a>Sintaxe


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolFamily* \[ no\]
</dt> <dd>

Especifica para qual tipo de rede obter informações de rota, por exemplo, IP ou IPX.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será a contagem de rede, o número de redes conhecidas para os protocolos de roteamento da família de protocolos especificada.

Se o valor de retorno for zero, nenhuma rota estará disponível ou a operação falhará. Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações.



| Valor                                                                                                    | Descrição                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEM \_ erros**</dt> </dl>                 | A operação foi bem-sucedida, mas não há rotas disponíveis.<br/>                                             |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl> | O valor do parâmetro *ProtocolFamily* não corresponde a nenhuma família de protocolos instalada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[Identificadores da família de protocolos RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

