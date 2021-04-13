---
title: Função MrmIndexFile (MrmResourceIndexer. h)
description: Indexa um arquivo de recurso que pertence a um aplicativo UWP. Usa uma lista explícita (mas opcional) de qualificadores de recursos. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
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
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455789"
---
# <a name="mrmindexfile-function"></a>Função MrmIndexFile

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Indexa um arquivo de recurso que pertence a um aplicativo UWP. Usa uma lista explícita (mas opcional) de qualificadores de recursos. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*indexador* \[ no\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos que indexará o arquivo de recurso.

</dd> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

O URI de recurso a ser atribuído ao recurso. O caminho será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.

</dd> <dt>

*FilePath* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho relativo para um arquivo que contém um recurso que você deseja indexar. Esse caminho é relativo à raiz de projeto do aplicativo UWP para o qual você está gerando arquivos PRI. Essa raiz do projeto é o valor de *projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> <dt>

*qualificadores* \[ em, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Uma lista opcional de qualificadores de recursos, por exemplo, L "idioma-en-US \_ Scale-100 \_ contraste-Standard". Uma cadeia de caracteres vazia ou **nullptr** indica um recurso neutro. Os qualificadores de recursos *não* são inferidos de *ResourceURI* nem de *containerPath*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Se você quiser especificar quaisquer qualificadores de recursos, passe-os no parâmetro *Qualifiers* . Qualificadores de recursos *não* são inferidos de *ResourceURI* nem de *FilePath*.

O segmento de nome de arquivo de *ResourceURI* (não *FilePath*) é usado como o nome do recurso.

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

 

