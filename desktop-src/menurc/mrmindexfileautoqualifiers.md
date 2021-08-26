---
title: Função MrmIndexFileAutoQualifiers (MrmResourceIndexer. h)
description: Indexa um arquivo de recurso que pertence a um aplicativo UWP. Infere uma lista de qualificadores de recursos do parâmetro filePath. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de PRI (indexação de recursos de pacote) e sistemas de compilação personalizados.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menus de função MrmIndexFileAutoQualifiers e outros recursos
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10dbdb564f7e2d830d1edea59be6ca6f11b72d2650a937f96b6d305b6c7f61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886726"
---
# <a name="mrmindexfileautoqualifiers-function"></a>Função MrmIndexFileAutoQualifiers

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Indexa um arquivo de recurso que pertence a um aplicativo UWP. Infere uma lista de qualificadores de recursos do parâmetro *FilePath* . Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexador* \[ no\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos que indexará o arquivo de recurso.

</dd> <dt>

*FilePath* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho relativo para um arquivo que contém um recurso que você deseja indexar. Esse caminho é relativo à raiz de projeto do aplicativo UWP para o qual você está gerando arquivos PRI. Essa raiz do projeto é o valor de *projectRoot* que você passou para [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

O segmento de nome de arquivo de *FilePath* é usado como o nome do recurso; e qualificadores de recursos são derivados de seu caminho. Por exemplo, se você passar L "imagens \\ de-de" \\ escala-100 \\background.png "para *FilePath* , o indexador de recursos adicionará um recurso denominado" background.png "com qualificadores DE recursos" idioma-de-de "e" escala-100 ".

L "Files" será usado como o nome da subárvore do mapa de recursos para esse recurso quando você gerar posteriormente um arquivo PRI desse indexador de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

