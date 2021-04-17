---
description: Especifica um arquivo a ser assinado.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Estrutura de SIGNER_FILE_INFO
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
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766818"
---
# <a name="signer_file_info-structure"></a>Estrutura de informações do \_ arquivo de signatário \_

A estrutura de **\_ \_ informações do arquivo de signatário** especifica um arquivo a ser assinado.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

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

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do arquivo a ser assinado.

</dd> <dt>

**hFile**
</dt> <dd>

Um identificador aberto para o arquivo especificado pelo membro **pwszFileName** . Se esse membro contiver um identificador válido, esse identificador será usado para acessar o arquivo. Esse membro pode ser definido como **nulo**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de assunto do assinante \_**](signer-subject-info.md)
</dt> </dl>

 

 




