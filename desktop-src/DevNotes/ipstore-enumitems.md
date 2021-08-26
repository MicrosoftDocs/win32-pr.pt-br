---
description: Retorna o ponteiro de interface de um subtipo para enumerar itens no banco de dados de armazenamento protegido.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Método IPStore:: EnumItems (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0b0ea4976dcfdfe2a099362e9a937ac69144bd678965c6a308cb96fed2a3c88b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001506"
---
# <a name="ipstoreenumitems-method"></a>Método IPStore:: EnumItems

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Retorna o ponteiro de interface de um subtipo para enumerar itens no banco de dados de armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

Especifica se o tipo é local para o computador ou associado somente ao usuário de criação.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt> </dl>    | O armazenamento é mantido na seção usuário atual do registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt> </dl> | O armazenamento é mantido na seção máquina local do registro.<br/> |



 

</dd> <dt>

*pItemType* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do item a ser enumerado.

</dd> <dt>

*pItemSubtype* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o subtipo de dados do item a ser enumerado.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado: deve ser definido como zero.

</dd> <dt>

*ppEnum* \[ no\]
</dt> <dd>

Um ponteiro para um ponteiro para uma interface [**IEnumPStoreItems**](ienumpstoreitems.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **HRESULT**. Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
