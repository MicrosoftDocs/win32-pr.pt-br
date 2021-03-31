---
title: Função RtmGetRouteAge (RTM. h)
description: A função RtmGetRouteAge retorna a idade de uma rota. A idade é o tempo, em segundos, desde que foi criada ou atualizada pela última vez.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- Função RtmGetRouteAge RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644820"
---
# <a name="rtmgetrouteage-function"></a>Função RtmGetRouteAge

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmGetRouteAge** retorna a idade de uma rota. A idade é o tempo, em segundos, desde que foi criada ou atualizada pela última vez.

## <a name="syntax"></a>Sintaxe


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Rota* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura específica de família de protocolos que especifica os dados de rota obtidos recentemente do Gerenciador de tabelas de roteamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um dos valores a seguir.



| Valor                                                                                   | Descrição                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Rota**</dt> </dl> | O tempo em segundos desde que uma rota foi criada ou atualizada pela última vez.<br/>                                                                                    |
| <dl> <dt>**INFINITE**</dt> </dl> | O conteúdo da estrutura de rota é inválido. Nesse caso, uma chamada para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um \_ parâmetro inválido de erro \_ .<br/> |



 

## <a name="remarks"></a>Comentários

A idade da rota é computada do \_ membro de carimbo de data/hora RR da estrutura que é apontada pelo parâmetro *Route* . O Gerenciador de tabela de roteamento define o valor desse membro quando uma rota é adicionada ou atualizada.

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

[Referência da versão 1 do Gerenciador de tabela de roteamento \_](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_rota de IP RTM \_**](rtm-ip-route.md)
</dt> <dt>

[**\_rota IPX do RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

