---
description: Especifica um assunto a ser assinado.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Estrutura de SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811787"
---
# <a name="signer_subject_info-structure"></a>Estrutura de informações de \_ assunto do assinante \_

A estrutura de **\_ \_ informações da entidade do assinante** especifica um assunto a ser assinado.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**pdwIndex**
</dt> <dd>

Este membro está reservado. Ele deve ser definido como zero.

</dd> <dt>

**dwSubjectChoice**
</dt> <dd>

Especifica se o assunto é um arquivo ou um [*blob*](../secgloss/b-gly.md). Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                         | Significado                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**Signatário \_ \_Blob de assunto**</dt> <dt>2 (0x2)</dt> </dl> | O assunto é um BLOB.<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**Signatário \_ \_Arquivo de assunto**</dt> <dt>1 (0x1)</dt> </dl> | O assunto é um arquivo.<br/> |



 

</dd> <dt>

**pSignerFileInfo**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações do arquivo de signatário**](signer-file-info.md) que especifica o arquivo a ser assinado.

</dd> <dt>

**pSignerBlobInfo**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de blob de assinante**](signer-blob-info.md) que especifica o blob a assinar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
