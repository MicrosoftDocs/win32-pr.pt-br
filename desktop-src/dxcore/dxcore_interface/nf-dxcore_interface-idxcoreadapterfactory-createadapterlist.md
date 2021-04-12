---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Gera uma lista de objetos de adaptador que representam o estado atual do adaptador do sistema e atendendo aos critérios especificados.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454222"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a>Método IDXCoreAdapterFactory:: createadapterlist

Gera uma lista de objetos de adaptador que representam o estado atual do adaptador do sistema e atendendo aos critérios especificados. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

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

O número de elementos na matriz apontados pelo argumento *FilterAttributes* .

### <a name="filterattributes-in"></a>filterAttributes [in]

Tipo: **GUID \* const**

Um ponteiro para uma matriz de GUIDs de atributo de adaptador. Para obter uma lista de GUIDs de atributo, consulte [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md). Pelo menos um GUID deve ser fornecido. Caso mais de um GUID seja fornecido na matriz, somente os adaptadores que atendem a *todos* os atributos solicitados serão incluídos na lista retornada.

### <a name="riid"></a>riid

Tipo: **REFIID**

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvAdapterList*. Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).

### <a name="ppvadapterlist-out"></a>ppvAdapterList [saída]

Tipo: **void \* \***

O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* . Após o retorno bem-sucedido, *\* ppvAdapterList* (o endereço desreferenciado) contém um ponteiro para a lista de adaptadores criada.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|E_INVALIDARG|`nullptr` foi fornecido para *FilterAttributes*, ou o 0 foi fornecido para *numAttributes*.|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid*.|
|E_POINTER|`nullptr` foi fornecido para *ppvAdapterList*.|

## <a name="remarks"></a>Comentários

Mesmo que nenhum adaptador seja encontrado, desde que os argumentos sejam válidos, **Createadapterlist** cria um objeto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) válido e retorna **S_OK**. Depois de gerado, os adaptadores nesta lista específica não serão alterados. Mas a lista será considerada obsoleta se um dos adaptadores se tornar inválidos posteriormente, ou se um novo adaptador chegar e atender aos critérios de filtro fornecidos. A lista retornada por **Createadapterlist** não é ordenada de nenhuma forma específica, mas a ordenação de uma lista é consistente em várias chamadas e até mesmo entre as reinicializações do sistema operacional. A ordenação pode ser alterada nas alterações de configuração do sistema, incluindo a adição ou remoção de um adaptador ou uma atualização de driver em um adaptador existente. Você pode se registrar para essas alterações com [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) usando o tipo de notificação **DXCoreNotificationType. AdapterListStale**.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)