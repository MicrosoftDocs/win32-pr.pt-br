---
title: Função MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer. h)
description: Indexa os recursos de cadeia de caracteres contidos dentro de um arquivo de recursos (. resw/. resjson) ou um. priinfo ou. prifile, pertencente a um aplicativo UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menus de função MrmIndexResourceContainerAutoQualifiers e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812324"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>Função MrmIndexResourceContainerAutoQualifiers

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Indexa os recursos de cadeia de caracteres contidos dentro de um arquivo de recursos (. resw/. resjson) ou um. priinfo ou. prifile, pertencente a um aplicativo UWP. Infere uma lista de qualificadores de recursos do parâmetro *containerPath* . Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexador* \[ no\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos que indexará os recursos de cadeia de caracteres.

</dd> <dt>

*containerPath* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho relativo para um. resw,. resjson,. priinfo ou. prifile que contém recursos de cadeia de caracteres que você deseja indexar. Esse caminho é relativo à raiz de projeto do aplicativo UWP para o qual você está gerando arquivos PRI. Essa raiz do projeto é o valor de *projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Os qualificadores de recursos são inferidos de *containerPath*. Por exemplo, um valor de L "en-US \\ \\ Resources. resw" adiciona recursos de cadeia de caracteres com o qualificador "Language-en-US".

O nome do arquivo de recursos será usado como o nome da subárvore do mapa de recursos para esses recursos quando você gerar posteriormente um arquivo PRI desse indexador de recursos.

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

 

