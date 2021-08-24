---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Gera uma lista de objetos de adaptador que representam o estado atual do adaptador do sistema e a atender aos critérios especificados.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0d00cba3236bf63a1691473098b1f94438b790a93a75215e36690745ee7977fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842516"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>Método IDXCoreAdapterFactory::CreateAdapterList

Gera uma lista de objetos de adaptador que representam o estado atual do adaptador do sistema e a atender aos critérios especificados. Para obter diretrizes de programação e exemplos de código, consulte [Usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a>Parâmetros

### <a name="numattributes"></a>numAttributes

Tipo: **uint32_t**

O número de elementos na matriz apontado pelo *argumento filterAttributes.*

### <a name="filterattributes-in"></a>filterAttributes [in]

Tipo: **const \* GUID**

Um ponteiro para uma matriz de GUIDs de atributo de adaptador. Para ver uma lista de GUIDs de atributo, consulte GUIDs de atributo do adaptador [DXCore.](../dxcore-adapter-attribute-guids.md) Pelo menos um GUID deve ser fornecido. Caso mais de um GUID seja fornecido na matriz,  somente os adaptadores que atendem a todos os atributos solicitados serão incluídos na lista retornada.

### <a name="riid"></a>riid

Tipo: **REFIID**

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvAdapterList.* Espera-se que esse seja o IID (identificador de interface) de [IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)

### <a name="ppvadapterlist-out"></a>ppvAdapterList [out]

Tipo: **\* \* void**

O endereço de um ponteiro para uma interface com a IID especificada no *parâmetro riid.* Após o retorno bem-sucedido, *\* ppvAdapterList* (o endereço desreferenciado) contém um ponteiro para a lista de adaptadores criada.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valor retornado|Descrição|
|-|-|
|E_INVALIDARG|`nullptr`foi fornecido *para filterAttributes* ou 0 foi fornecido para *numAttributes.*|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid.*|
|E_POINTER|`nullptr`foi fornecido para *ppvAdapterList.*|

## <a name="remarks"></a>Comentários

Mesmo se nenhum adaptador for encontrado, desde que os argumentos sejam válidos, **CreateAdapterList** criará um objeto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) válido e retornará **S_OK**. Depois de gerados, os adaptadores nesta lista específica não mudarão. Mas a lista será considerada desleada se um dos adaptadores posteriormente se tornar inválido ou se um novo adaptador chegar que atenda aos critérios de filtro fornecidos. A lista retornada por **CreateAdapterList** não é ordenada de nenhuma maneira específica, mas a ordenação de uma lista é consistente em várias chamadas e até mesmo em reinicializações do sistema operacional. A ordenação pode mudar após alterações de configuração do sistema, incluindo a adição ou remoção de um adaptador ou uma atualização de driver em um adaptador existente. Você pode se registrar para essas alterações [com IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) usando o tipo de notificação **DXCoreNotificationType.AdapterListStale**.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [Referência de DXCore,](../dxcore-reference.md)GUIDs de atributo de adaptador [DXCore,](../dxcore-adapter-attribute-guids.md)usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)