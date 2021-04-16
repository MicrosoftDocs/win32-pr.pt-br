---
description: O método SetBandwidthInfo define as informações de largura de banda.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Método ITConnection:: SetBandwidthInfo (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779905"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>Método ITConnection:: SetBandwidthInfo

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SetBandwidthInfo** define as informações de largura de banda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pModifier* \[ no\]
</dt> <dd>

Ponteiro para um **BSTR** que indica o escopo da largura de banda que está sendo definida. Para obter mais informações, consulte a seção Comentários a seguir.

</dd> <dt>

*Largura de banda* \[ no\]
</dt> <dd>

Larga.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pModifier* ou *Bandwidth* não é válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>   |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                     |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                    |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PModifier* e usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.

Referência: RFC 2327.

O modificador de largura de banda normalmente será o CT ou como:

**Total da conferência CT:** Uma largura de banda máxima implícita é associada [*a cada TTL*](t-tapgloss.md) (vida útil) no MBone ou dentro de uma região de escopo administrativo de multicast específica (a largura de banda MBone versus os limites de TTL são fornecidos nas perguntas frequentes sobre o MBone). Se a largura de banda de uma sessão ou mídia em uma sessão for diferente da largura de banda implícita do escopo, a \` b = CT:... ' a linha deve ser fornecida para a sessão, fornecendo o limite superior proposto à largura de banda usada. A principal finalidade disso é dar uma ideia aproximada de se duas ou mais conferências podem coexistir simultaneamente.

**Máximo de Application-Specific:** A largura de banda é interpretada para ser específica ao aplicativo, ou seja, será o conceito de largura de banda máxima do aplicativo. Normalmente, isso coincidirá com o que está definido no controle "máximo de largura de banda" do aplicativo, se aplicável.

Observe que a CT fornece uma figura de largura de banda total para todas as mídias em todos os sites. COMO o fornece uma figura de largura de banda para uma única mídia em um único site, embora possa haver muitos sites enviando simultaneamente.

**Mecanismo de extensão:** Os escritores de ferramenta podem definir modificadores de largura de banda experimentais prefixando seus modificadores com "X-".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

