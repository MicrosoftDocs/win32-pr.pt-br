---
title: Função MrmCreateResourceIndexerFromPreviousSchemaFile (MrmResourceIndexer.h)
description: Cria um indexador de recursos de um arquivo de esquema criado com uma chamada anterior para MrmDumpPriFile. Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de build personalizados.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menus da função MrmCreateResourceIndexerFromPreviousSchemaFile e outros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622fe76c9206b4a8223d27d810f3d02bc0dca1d08730623b595ead24eab719d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847366"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a>Função MrmCreateResourceIndexerFromPreviousSchemaFile

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Cria um indexador de recursos de um arquivo de esquema criado com uma chamada anterior para [**MrmDumpPriFile.**](mrmdumpprifile.md) Para obter mais informações e passo a passo baseado em cenário de como usar essas APIs, consulte [APIs de PRI (indexação](/windows/uwp/app-resources/pri-apis-custom-build-systems)de recursos de pacote) e sistemas de build personalizados .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*projectRoot* \[ Em\]
</dt> <dd>

Tipo: **PCWSTR**

A raiz do projeto do aplicativo UWP para o qual você gerará arquivos PRI. Em outras palavras, o caminho para os arquivos de recurso desse aplicativo. Especifique isso para que você possa especificar caminhos relativos a essa raiz nas chamadas à API subsequentes para o mesmo indexador de recursos.

</dd> <dt>

*platformVersion* \[ Em\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

A versão da plataforma de destino para o indexador de recursos.

</dd> <dt>

*defaultQualifiers* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Uma lista de qualificadores de recurso padrão. Por exemplo, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*schemaFile* \[ Em\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho de arquivo completo para um arquivo de esquema criado por uma chamada anterior para [**MrmDumpPriFile.**](mrmdumpprifile.md)

</dd> <dt>

*indexador* \[ in, out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Um ponteiro para um alça do indexador de recursos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função tiver êxito, caso contrário, algum outro valor. Use as macros SUCCEEDED() ou FAILED() (definidas em winerror.h) para determinar o êxito ou a falha.

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

 

