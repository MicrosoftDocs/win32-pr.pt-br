---
description: Abre um item para vários acessos.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Método IPStore:: OpenItem (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751038"
---
# <a name="ipstoreopenitem-method"></a>Método IPStore:: OpenItem

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Abre um item para vários acessos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
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

Um ponteiro para um GUID que identifica o tipo de dados do item a ser aberto.

</dd> <dt>

*pItemSubtype* \[ no\]
</dt> <dd>

Um ponteiro para um GUID que indica o subtipo de item a ser aberto.

</dd> <dt>

*szItemName* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do item a ser aberto.

</dd> <dt>

*ModeFlags* \[ no\]
</dt> <dd>

Descreve os modos de acesso aos quais um conjunto especificado de cláusulas de acesso pertence. Para obter mais informações, consulte [**Pstore Types**](pstore-types.md).



| Valor                                                                                                                                                                                                         | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ LER**</dt> <dt>0x0001</dt> </dl>    | Modo de acesso de leitura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_**</dt> <dt>0X0002</dt> de gravação </dl> | Modo de acesso de gravação.<br/> |



 

</dd> <dt>

*pProomptInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado: deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **HRESULT** . Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.

## <a name="remarks"></a>Comentários

Usar **OpenItem** para abrir um item no banco de dados de armazenamento protegido requer que ele eventualmente seja fechado usando [**IPStore:: CloseItem**](ipstore-closeitem.md) para evitar um vazamento de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**\_PROMPTINFO PST**](pst-promptinfo.md)
</dt> </dl>

 

 
