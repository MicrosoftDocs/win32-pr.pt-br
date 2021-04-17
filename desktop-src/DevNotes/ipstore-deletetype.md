---
description: Exclui um tipo especificado do banco de dados de armazenamento protegido.
ms.assetid: 5e3a08eb-e16b-4d9f-82be-241eb3137d17
title: 'IPStore: método eleteType de:D (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7833dd59a10b0194347e906d5c5a4711585dea14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755920"
---
# <a name="ipstoredeletetype-method"></a>IPStore: método eleteType de:D

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Exclui um tipo especificado do banco de dados de armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteType(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in]       DWORD   dwFlags
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

*pType* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado: deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **HRESULT** . Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
