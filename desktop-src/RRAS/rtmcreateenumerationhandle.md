---
title: Função RtmCreateEnumerationHandle (RTM. h)
description: A função RtmCreateEnumerationHandle retorna um identificador a ser usado com RtmEnumerateGetNextRoute para examinar todas as rotas ou um subconjunto de rotas, conhecido pelo Gerenciador de tabelas de roteamento.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- Função RtmCreateEnumerationHandle RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085281"
---
# <a name="rtmcreateenumerationhandle-function"></a>Função RtmCreateEnumerationHandle

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmCreateEnumerationHandle** retorna um identificador a ser usado com [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) para examinar todas as rotas ou um subconjunto de rotas, conhecido pelo Gerenciador de tabelas de roteamento.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolFamily* \[ no\]
</dt> <dd>

Especifica a família de protocolos das rotas a serem enumeradas.

</dd> <dt>

*EnumerationFlags* \[ no\]
</dt> <dd>

Especifica quais rotas devem ser enumeradas. Esse parâmetro limita o conjunto de rotas retornado pela API de enumeração a um subconjunto definido pelos seguintes sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* . Esse parâmetro pode usar um dos valores a seguir.



| EnumerationFlags                                                                                                                                                                              | Significado                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**\_somente RTM \_ desta \_ rede**</dt> </dl>       | Enumere somente as rotas que têm o mesmo número de rede que o \_ membro de rede RR da estrutura apontada por CriteriaRoute.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**RTM \_ somente \_ esta \_ interface**</dt> </dl> | Enumere somente as rotas que foram obtidas por meio da interface especificada pelo campo do RR \_ InterfaceName da estrutura apontada por CriteriaRoute.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**RTM \_ somente \_ esse \_ protocolo**</dt> </dl>    | Enumere somente as rotas que foram adicionadas pelo protocolo de roteamento especificado pelo \_ campo RR RoutingProtocol da estrutura apontada por CriteriaRoute.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**\_somente \_ as melhores \_ rotas do RTM**</dt> </dl>          | Enumere apenas as melhores rotas para cada uma das redes no conjunto.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de rota específica da família de protocolos [**( \_ \_ rota de IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)). Os valores de membro nessa estrutura correspondem aos sinalizadores especificados pelo parâmetro *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um **identificador** a ser usado com as chamadas de enumeração subsequentes.

Se a função falhar ou não houver rotas com os critérios especificados, o valor de retorno será **nulo**. Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações.



| Valor                                                                                                       | Descrição                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRO \_ sem \_ rotas**</dt> </dl>            | Não há rotas com os critérios especificados.<br/>                                                             |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>    | Um ou mais dos parâmetros de entrada são inválidos (por exemplo, família de protocolos desconhecida, sinalizadores de enumeração inválidos).<br/> |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/>                                                      |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl>   | Memória insuficiente para alocar o identificador.<br/>                                                              |



 

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

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_rota de IP RTM \_**](rtm-ip-route.md)
</dt> <dt>

[**\_rota IPX do RTM \_**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

