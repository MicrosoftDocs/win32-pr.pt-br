---
title: Função RtmIsRoute (Rtm.h)
description: A função RtmIsRoute determina se uma ou mais rotas para uma rede de destino especificada existem. Nesse caso, a função retorna informações para a melhor rota para essa rede.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Função RtmIsRoute RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312b43a7cf66e17cc6016fe3ad35bd21cd1e7ae19ecd7864a10de4d977a92ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073806"
---
# <a name="rtmisroute-function"></a>Função RtmIsRoute

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

A **função RtmIsRoute** determina se uma ou mais rotas para uma rede de destino especificada existem. Nesse caso, a função retorna informações para a melhor rota para essa rede.

## <a name="syntax"></a>Sintaxe


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolFamily* \[ Em\]
</dt> <dd>

Especifica o tipo de estrutura de dados apontado pelo *parâmetro Network,* por exemplo, [**IP \_ NETWORK**](ip-network.md), [**IPX \_ NETWORK.**](ipx-network.md)

</dd> <dt>

*Rede* \[ Em\]
</dt> <dd>

Ponteiro para uma estrutura que especifica dados de número de rede específicos da família de protocolo. Esses dados identificam a rede para a qual o chamador busca informações de rota.

</dd> <dt>

*BestRoute* \[ out\]
</dt> <dd>

Ponteiro para uma estrutura específica da família de protocolos que recebe as melhores informações de rota atuais, se alguma.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um dos códigos a seguir.



| Valor                                                                                                       | Descrição                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Verdade**</dt> </dl>                         | Existe pelo menos uma rota para a rede especificada. A melhor rota é retornada na estrutura apontada pelo *parâmetro BestRoute.*<br/>      |
| <dl> <dt>**False**</dt> </dl>                        | Não há nenhuma rota para a rede especificada ou a operação falhou. Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações:<br/> |
| <dl> <dt>**NENHUM \_ ERRO**</dt> </dl>                    | A operação foi bem-sucedida, mas não há nenhuma rota para a rede especificada.<br/>                                                                      |
| <dl> <dt>**ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl>    | O valor do parâmetro *ProtocolFamily* não corresponde a nenhuma família de protocolo instalada.<br/>                                             |
| <dl> <dt>**ERRO \_ NENHUM RECURSO DO \_ \_ SISTEMA**</dt> </dl> | Não há recursos suficientes para executar a operação.<br/>                                                                                  |



 

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

[**Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**REDE \_ IP**](ip-network.md)
</dt> <dt>

[**REDE \_ IPX**](ipx-network.md)
</dt> <dt>

[Identificadores de família de protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

