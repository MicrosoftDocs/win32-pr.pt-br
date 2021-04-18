---
description: Configura a preferência dos recursos padrão.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'Método IH323LineEx:: SetDefaultCapabilityPreferrence (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756997"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>Método IH323LineEx:: SetDefaultCapabilityPreferrence

\[O **SetDefaultCapabilityPreferrence** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **SetDefaultCapabilityPreferrence** configura a preferência dos recursos padrão. Os recursos têm um peso padrão de 100. Se o aplicativo especificar um peso mais alto para um recurso, ele terá uma prioridade mais alta durante a negociação H. 245. Se o aplicativo definir o peso de um recurso como 0, ele não será usado na negociação H. 245.

Esse método é cumulativo. Por exemplo, se esse método for chamado primeiro para desabilitar um recurso e for chamado novamente para desabilitar outro, ambos os recursos serão desabilitados como resultado dessas duas chamadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwNumCaps* \[ no\]
</dt> <dd>

Um valor **DWORD** que contém o número de recursos definidos com este método.

</dd> <dt>

*pCapabilities* \[ no\]
</dt> <dd>

Uma matriz de recursos. Cada elemento da matriz é um valor [**de \_ recurso H245**](h245-capability.md) .

</dd> <dt>

*pWeights* \[ no\]
</dt> <dd>

Uma matriz de pesos associada aos recursos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pCapabilities* é **nulo** ou o parâmetro *pWeights* é **nulo** ou *pCapabilities* e *pWeights* são **nulos** ou a matriz pCapabilities contém um objeto de recurso H. 245 inválido.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Não é possível ler um elemento da matriz *pWeights* ou de um elemento da matriz *pCapabilities* .<br/>                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




