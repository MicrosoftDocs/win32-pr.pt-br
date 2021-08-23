---
description: Especifica um arquivo a ser assinar.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b0bb1bce810d87d70e05284e3d13942c5e2e49d07bd2d829c3839f793ae6a061
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898822"
---
# <a name="signer_file_info-structure"></a>Estrutura DE \_ INFORMAÇÕES DE ARQUIVO DO \_ SIGNER

A **estrutura SIGNER \_ FILE \_ INFO** especifica um arquivo a ser assinar.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de header. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**pwszFileName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do arquivo a assinar.

</dd> <dt>

**Hfile**
</dt> <dd>

Um handle aberto para o arquivo especificado pelo **membro pwszFileName.** Se esse membro contiver um handle válido, esse handle será usado para acessar o arquivo. Esse membro pode ser definido como **NULL.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DE \_ ASSUNTO DO \_ SIGNER**](signer-subject-info.md)
</dt> </dl>

 

 




