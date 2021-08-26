---
description: Exclui um subtipo especificado de dentro do tipo especificado.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: Método IPStore::D eleteSubtype (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 88bb437c89073f3601050c1246f1e59b136a85955da4697d338077343a4d1bc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001606"
---
# <a name="ipstoredeletesubtype-method"></a>Método IPStore::D eleteSubtype

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Exclui um subtipo especificado de dentro do tipo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
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

*pType* \[ Em\]
</dt> <dd>

Um ponteiro para um GUID que identifica o tipo de dados do armazenamento.

</dd> <dt>

*pSubtype* \[ Em\]
</dt> <dd>

Um ponteiro para um GUID que identifica o subtipo de dados do armazenamento.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Reservado: deve ser definido como zero.

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

 

 
