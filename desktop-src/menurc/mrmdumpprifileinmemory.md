---
title: Função MrmDumpPriFileInMemory (MrmResourceIndexer. h)
description: Despeja um arquivo PRI (que é binário) para seu equivalente XML (como dados na memória), a fim de torná-lo mais fácil de ser lido.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menus de função MrmDumpPriFileInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c591f95b772d71fd0ce614598bbf793d84dff70a0c29664da460c8be33569d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092146"
---
# <a name="mrmdumpprifileinmemory-function"></a>Função MrmDumpPriFileInMemory

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Despeja um arquivo PRI (que é binário) para seu equivalente XML (como dados na memória), a fim de torná-lo mais fácil de ser lido. A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*. Chame [**MrmFreeMemory**](mrmfreememory.md) com o mesmo ponteiro para liberar essa memória. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexFileName* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho de arquivo completo para um arquivo PRI. Esse é o arquivo PRI que será despejado em XML.

</dd> <dt>

*schemaPriFile* \[ em, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Um caminho de arquivo completo opcional para um arquivo de esquema (ou para um arquivo PRI que representa um esquema; consulte comentários).

</dd> <dt>

*dumptype* \[ no\]
</dt> <dd>

Tipo: **[ **MrmDumpType**](mrmdumptype.md)**

Especifica o quão detalhado o despejo de XML deve ser ou se um esquema deve ser despejado.

</dd> <dt>

*outputXmlData* \[ fora\]
</dt> <dd>

Tipo: **byte \* \***

O endereço de um ponteiro para BYTE. A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*. Chame [**MrmFreeMemory**](mrmfreememory.md) com o ponteiro para byte para liberar essa memória.

</dd> <dt>

*outputXmlSize* \[ fora\]
</dt> <dd>

Tipo: **ULONG \***

O endereço de um ULONG. No *outputXmlSize*, a função retorna o tamanho da memória alocada apontada por *outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Um pacote de recursos sem esquema é aquele criado com o argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passado para [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou com a opção *omitSchemaFromResourcePacks* no arquivo de configuração PRI). Para despejar um pacote de recursos sem esquema, passe o caminho para os dados PRI do pacote principal como o argumento para o parâmetro *schemaPriFile* .

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

 

