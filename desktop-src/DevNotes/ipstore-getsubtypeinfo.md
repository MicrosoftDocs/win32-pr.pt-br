---
description: Recupera informações associadas a um subtipo.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'Método IPStore:: GetSubtypeInfo (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d97b1f710344acf2c635adb5109175d017fc568d87673f5565e1be5b22e06cf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749836"
---
# <a name="ipstoregetsubtypeinfo-method"></a>Método IPStore:: GetSubtypeInfo

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Recupera informações associadas a um subtipo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

A área de armazenamento do provedor.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt> </dl>    | O armazenamento é mantido na seção usuário atual do registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt> </dl> | O armazenamento é mantido na seção máquina local do registro.<br/> |



 

</dd> <dt>

*pType* \[ no\]
</dt> <dd>

Um ponteiro para um GUID que identifica o tipo de dados do armazenamento.

</dd> <dt>

*pSubtype* \[ no\]
</dt> <dd>

Um ponteiro para um GUID que identifica o subtipo de dados do armazenamento.

</dd> <dt>

*ppInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ TYPEINFO de PST**](pst-typeinfo.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado: deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um valor **HRESULT** . Um valor de PST \_ E \_ OK indica que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**TYPEINFO de PST \_**](pst-typeinfo.md)
</dt> </dl>

 

 
