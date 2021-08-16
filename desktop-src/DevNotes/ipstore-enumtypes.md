---
description: Retorna uma interface para enumerar tipos que estão atualmente registrados no banco de dados protegido.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: Método IPStore::EnumTypes (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: c44429b4145158bc54e52d700546a29caf3e9665d38e51679e596adbdec6c3b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827109"
---
# <a name="ipstoreenumtypes-method"></a>Método IPStore::EnumTypes

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Retorna uma interface para enumerar tipos que estão atualmente registrados no banco de dados protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

Especifica se o tipo é local para o computador ou associado somente ao usuário que está criando.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ ATUAL \_ DO USUÁRIO**</dt> <dt>0X00000000</dt> </dl>    | O armazenamento é mantido na seção de usuário atual do Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHAVE \_ DO \_ COMPUTADOR LOCAL**</dt> <dt>0X00000001</dt> </dl> | O armazenamento é mantido na seção computador local do Registro.<br/> |



 

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Reservado: deve ser definido como zero.

</dd> <dt>

*ppenum* \[ Em\]
</dt> <dd>

Um ponteiro para uma interface [**IEnumPStoreTypes**](ienumpstoretypes.md) usada para executar as tarefas de enumeração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **valor HRESULT.** Um valor de **PST \_ E OK \_ indica** que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
