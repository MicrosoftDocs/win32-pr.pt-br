---
title: Função MrmPeekResourceIndexerMessages (MrmResourceIndexer. h)
description: Exiba todas as mensagens geradas por um indexador de recursos. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
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
ms.openlocfilehash: 45599865633afa413594be7e82b0c7ace853434b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009430"
---
# <a name="mrmpeekresourceindexermessages-function"></a>Função MrmPeekResourceIndexerMessages

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Exiba todas as mensagens geradas por um indexador de recursos. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*indexador* \[ no\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos que as mensagens que você deseja exibir.

</dd> <dt>

*mensagens* \[ do fora\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

Um ponteiro para um ponteiro para um [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md). A função aloca uma matriz de **MrmResourceIndexerMessage** e retorna um ponteiro para essa memória em *mensagens*. Não libere o ponteiro cujo endereço você passa para *as mensagens*.

</dd> <dt>

*numMsgs* \[ fora\]
</dt> <dd>

Tipo: **ULONG \** _

O número de mensagens retornadas em _messages *.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Seu aplicativo não possui a memória alocada e retornada em *mensagens*, portanto, não a libere.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

