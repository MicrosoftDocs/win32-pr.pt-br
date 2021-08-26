---
title: Função MrmCreateResourceFileInMemory (MrmResourceIndexer.h)
description: Cria informações de PRI como um blob na memória, não como um arquivo em disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menus de função MrmCreateResourceFileInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff34ddaab25f47f537c1270ad3a70719a43e2e1efa978fbad19cbe9ae77ba937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886746"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>Função MrmCreateResourceFileInMemory

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Cria informações de PRI como um blob na memória, não como um arquivo em disco. A função aloca memória e retorna um ponteiro para essa memória em *outputPriData*. Chame [**MrmFreeMemory com**](mrmfreememory.md) o mesmo ponteiro para liberar essa memória. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexador* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos do qual criar as informações do PRI.

</dd> <dt>

*packagingMode* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Especifica se as informações do PRI devem ser autônomas ou um pacote de recursos. **Não há suporte para MrmPackagingModeAutoSplit.**

</dd> <dt>

*packagingOptions* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Especifica opções adicionais sobre as informações do PRI.

</dd> <dt>

*outputPriData* \[ out\]
</dt> <dd>

Tipo: **BYTE \* \***

O endereço de um ponteiro para BYTE. A função aloca memória e retorna um ponteiro para essa memória em *outputPriData*. Chame [**MrmFreeMemory com**](mrmfreememory.md) o ponteiro para BYTE para liberar essa memória.

</dd> <dt>

*outputPriSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

O endereço de um ULONG. Em *outputPriSize*, a função retorna o tamanho da memória alocada apontada por *outputPriData*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função tiver êxito, caso contrário, algum outro valor. Use as macros SUCCEEDED() ou FAILED() (definidas em winerror.h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Se você passar *outputPriData* para [**MrmCreateResourceIndexerFromPreviousPriData,**](mrmcreateresourceindexerfrompreviouspridata-.md)não liberará a memória até terminar de usar o indexador de recursos.

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

 

