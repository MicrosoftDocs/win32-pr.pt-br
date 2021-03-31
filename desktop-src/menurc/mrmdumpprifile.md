---
title: Função MrmDumpPriFile (MrmResourceIndexer. h)
description: Despeja um arquivo PRI (que é binário) para seu equivalente XML (como um arquivo no disco) para torná-lo mais fácil de ler.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menus de função MrmDumpPriFile e outros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644731"
---
# <a name="mrmdumpprifile-function"></a>Função MrmDumpPriFile

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Despeja um arquivo PRI (que é binário) para seu equivalente XML (como um arquivo no disco) para torná-lo mais fácil de ler. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
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

*outputXmlFile* \[ no\]
</dt> <dd>

Tipo: **PCWSTR**

O caminho de um arquivo XML a ser criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="remarks"></a>Comentários

Um pacote de recursos sem esquema é aquele criado com o argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passado para [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou com a opção *omitSchemaFromResourcePacks* no arquivo de configuração PRI). Para despejar um pacote de recursos sem esquema, passe o caminho para os dados PRI do pacote principal como o argumento para o parâmetro *schemaPriFile* .

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

 

