---
title: Função MrmDumpPriDataInMemory (MrmResourceIndexer. h)
description: Despeja informações de PRI (como um blob na memória, criado por uma chamada anterior para MrmCreateResourceFileInMemory) para seu equivalente XML (como dados na memória), para torná-la mais fácil de ler.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menus de função MrmDumpPriDataInMemory e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759015"
---
# <a name="mrmdumppridatainmemory-function"></a>Função MrmDumpPriDataInMemory

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Despeja informações de PRI (como um blob na memória, criado por uma chamada anterior para [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) para seu equivalente XML (como dados na memória), para torná-la mais fácil de ler. A função aloca memória e retorna um ponteiro para essa memória em *outputXmlData*. Chame [**MrmFreeMemory**](mrmfreememory.md) com o mesmo ponteiro para liberar essa memória. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inputPriData* \[ no\]
</dt> <dd>

Tipo: **byte \** _

Um ponteiro para dados PRI criados por uma chamada anterior para [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md).

</dd> <dt>

*inputPriSize* \[ no\]
</dt> <dd>

Tipo: **ULONG**

O tamanho dos dados apontados por *inputPriData*.

</dd> <dt>

*schemaPriData* \[ em, opcional\]
</dt> <dd>

Tipo: **byte \** _

Um ponteiro opcional para informações de PRI (como um blob na memória) que representa os dados de esquema criados por uma chamada anterior para [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md). Não libere *schemaPriData* até terminar de usar o indexador de recursos. Consulte também comentários.

</dd> <dt>

*schemaPriSize* \[ no\]
</dt> <dd>

Tipo: **ULONG**

O tamanho dos dados apontados por *schemaPriData*.

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

Tipo: **ULONG \** _

O endereço de um ULONG. No _outputXmlSize *, a função retorna o tamanho da memória alocada apontada por *outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Um pacote de recursos sem esquema é aquele criado com o argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passado para [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou com a opção *omitSchemaFromResourcePacks* no arquivo de configuração PRI). Para despejar um pacote de recursos sem esquema, passe o caminho para os dados PRI do pacote principal como o argumento para o parâmetro *schemaPriData* .

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

 

