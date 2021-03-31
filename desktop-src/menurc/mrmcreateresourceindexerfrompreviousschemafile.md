---
title: Função MrmCreateResourceIndexerFromPreviousSchemaFile (MrmResourceIndexer. h)
description: Cria um indexador de recurso a partir de um arquivo de esquema criado com uma chamada anterior para MrmDumpPriFile. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menus de função MrmCreateResourceIndexerFromPreviousSchemaFile e outros recursos
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
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645038"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a>Função MrmCreateResourceIndexerFromPreviousSchemaFile

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Cria um indexador de recurso a partir de um arquivo de esquema criado com uma chamada anterior para [**MrmDumpPriFile**](mrmdumpprifile.md). Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*projectRoot* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

A raiz do projeto do aplicativo UWP para o qual você irá gerar arquivos PRI. Em outras palavras, o caminho para os arquivos de recurso do aplicativo. Especifique isso para que você possa especificar caminhos relativos a essa raiz em chamadas de API subsequentes para o mesmo indexador de recursos.

</dd> <dt>

*platformVersion* \[ no\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

A versão da plataforma de destino para o indexador de recursos.

</dd> <dt>

*Defaultqualifiers* \[ em, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Uma lista de qualificadores de recurso padrão. Por exemplo, L "idioma-en-US \_ escala-100 \_ contraste-padrão"

</dd> <dt>

*esquema de esquemas* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho de arquivo completo para um arquivo de esquema criado por uma chamada anterior para [**MrmDumpPriFile**](mrmdumpprifile.md).

</dd> <dt>

*indexador* \[ entrada, saída\]
</dt> <dd>

Tipo: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Um ponteiro para um identificador de indexador de recurso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

