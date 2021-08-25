---
description: Configura a preferência dos recursos padrão.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: Método IH323LineEx::SetDefaultCapabilityPrefault (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64eb3385edb758529f27f9fb90eb0cce998eca60f202c72a28ba48a5318c6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992076"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>Método IH323LineEx::SetDefaultCapabilityPrefault

\[**SetDefaultCapabilityPrefault** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método SetDefaultCapabilityPrefault** configura a preferência dos recursos padrão. Os recursos têm um peso padrão de 100. Se o aplicativo especificar um peso mais alto para uma funcionalidade, ele terá uma prioridade mais alta durante a negociação H.245. Se o aplicativo define o peso de uma funcionalidade como 0, ele não será usado na negociação H.245.

Esse método é cumulativo. Por exemplo, se esse método for chamado primeiro para desabilitar uma funcionalidade e for chamado novamente para desabilitar outro, ambos os recursos serão desabilitados como resultado dessas duas chamadas.

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

*dwNumCaps* \[ Em\]
</dt> <dd>

Um **valor DWORD** que contém o número de funcionalidades definidas com esse método.

</dd> <dt>

*pCapabilities* \[ Em\]
</dt> <dd>

Uma matriz de recursos. Cada elemento da matriz é um [**valor H245 \_ CAPABILITY.**](h245-capability.md)

</dd> <dt>

*pWeights* \[ Em\]
</dt> <dd>

Uma matriz de pesos associada aos recursos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                                                                                                                                                                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pCapabilities* é **NULL** ou o parâmetro *pWeights* é **NULL** ou *pCapabilities* e *pWeights* são **NULL** ou a matriz pCapabilities contém um objeto de funcionalidade H.245 inválido.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Não é possível ler um elemento da matriz *pWeights* ou um elemento da *matriz pCapabilities.*<br/>                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




