---
title: Função MrmPeekResourceIndexerMessages (MrmResourceIndexer.h)
description: Exibir todas as mensagens geradas por um indexador de recursos. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de build personalizados.
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- Menus de função MrmPeekResourceIndexerMessages e outros recursos
topic_type:
- apiref
api_name:
- MrmPeekResourceIndexerMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f72325ab147656873af2bbf13d7ce1cfa47802c816dc9f14f0c6ee4f3c821683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847326"
---
# <a name="mrmpeekresourceindexermessages-function"></a>Função MrmPeekResourceIndexerMessages

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Exibir todas as mensagens geradas por um indexador de recursos. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmPeekResourceIndexerMessages(
  _In_  MrmResourceIndexerHandle  indexer,
  _Out_ MrmResourceIndexerMessage **messages,
  _Out_ ULONG                     *numMsgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexador* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos que as mensagens que você deseja exibir.

</dd> <dt>

*mensagens* \[ out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

Um ponteiro para um ponteiro para [**um MrmResourceIndexerMessage**](mrmresourceindexermessage.md). A função aloca uma matriz de **MrmResourceIndexerMessage** e retorna um ponteiro para essa memória nas *mensagens*. Não liberar o ponteiro cujo endereço você passa para *mensagens*.

</dd> <dt>

*numMsgs* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

O número de mensagens retornadas nas *mensagens*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função tiver êxito, caso contrário, algum outro valor. Use as macros SUCCEEDED() ou FAILED() (definidas em winerror.h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Seu aplicativo não tem a memória alocada e retornada nas mensagens *,* portanto, não a libera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do servidor\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

