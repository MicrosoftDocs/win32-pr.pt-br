---
title: Função MrmIndexFile (MrmResourceIndexer.h)
description: Indexa um arquivo de recurso que pertence a um aplicativo UWP. Utiliza uma lista explícita (mas opcional) de qualificadores de recursos. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de build personalizados.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menus de função MrmIndexFile e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004e8d81f3af7d0aa7844ed5661f71713db3f7fc49616fba0d56bed833a87f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733676"
---
# <a name="mrmindexfile-function"></a>Função MrmIndexFile

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, quanto às informações fornecidas aqui.\]

Indexa um arquivo de recurso que pertence a um aplicativo UWP. Utiliza uma lista explícita (mas opcional) de qualificadores de recursos. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
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

*filePath* \[ Em\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho relativo para um arquivo que contém um recurso que você deseja indexar. Esse caminho é relativo à raiz do projeto do aplicativo UWP para o qual você está gerando arquivos PRI. Essa raiz do projeto é o valor *de projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> <dt>

*qualificadores* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Uma lista opcional de qualificadores de recursos, por exemplo, L"language-en-US \_ scale-100 \_ contrast-standard". Uma cadeia de caracteres vazia **ou nullptr** indica um recurso neutro. Qualificadores de recursos não *são* inferidos de *resourceUri* nem de *containerPath.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função tiver êxito, caso contrário, algum outro valor. Use as macros SUCCEEDED() ou FAILED() (definidas em winerror.h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Se você quiser especificar qualificadores de recursos, passe-os no parâmetro *de qualificadores.* Qualificadores de recursos *não são* inferidos de *resourceUri* nem de *filePath*.

O segmento de nome de arquivo *de resourceUri* (não *filePath*) é usado como o nome do recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1803 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do servidor\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

