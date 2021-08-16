---
title: Função MrmIndexEmbeddedData (MrmResourceIndexer.h)
description: Indexa um único recurso de dados inseridos pertencente a um aplicativo UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Menus da função MrmIndexEmbeddedData e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7897df30506b66e74122c238e25a5b20fa5e1635e299c8a08db2519c842bdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971995"
---
# <a name="mrmindexembeddeddata-function"></a>Função MrmIndexEmbeddedData

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Indexa um único recurso **de dados inseridos** pertencente a um aplicativo UWP. Utiliza uma lista explícita (mas opcional) de qualificadores de recursos. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexador* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos que indexa o arquivo de recurso.

</dd> <dt>

*resourceUri* \[ Em\]
</dt> <dd>

Tipo: **PCWSTR**

O URI do recurso a ser atribuído ao recurso. O caminho será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.

</dd> <dt>

*embeddedData* \[ Em\]
</dt> <dd>

Tipo: **const \* BYTE**

Um ponteiro para os dados do recurso que você deseja indexar.

</dd> <dt>

*embeddedDataSize* \[ Em\]
</dt> <dd>

Tipo: **ULONG**

O tamanho dos dados apontados por *embeddedData.*

</dd> <dt>

*qualificadores* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Uma lista opcional de qualificadores de recursos, por exemplo, L"language-en-US \_ scale-100 \_ contrast-standard". Uma cadeia de caracteres vazia **ou nullptr** indica um recurso neutro. Qualificadores de recursos *não são* inferidos de *resourceUri.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função tiver êxito, caso contrário, algum outro valor. Use as macros SUCCEEDED() ou FAILED() (definidas em winerror.h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Se você quiser especificar qualificadores de recurso, passe-os no parâmetro *de qualificadores.* Qualificadores de recursos *não são* inferidos de *resourceUri.*

O segmento de nome de arquivo *de resourceUri* é usado como o nome do recurso.

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

 

