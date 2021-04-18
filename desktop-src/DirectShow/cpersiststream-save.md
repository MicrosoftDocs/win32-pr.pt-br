---
description: Salva os dados do filtro em um determinado fluxo.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Método CPersistStream. Save (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771844"
---
# <a name="cpersiststreamsave-method"></a>Método CPersistStream. Save

Salva os dados do filtro em um determinado fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStm* 
</dt> <dd>

Ponteiro para o fluxo no qual os dados serão salvos.

</dd> <dt>

*fClearDirty* 
</dt> <dd>

Sinalizador que indica se o sinalizador sujo do fluxo atual deve ser redefinido; **Verdadeiro** significa redefini-lo. (Quando o método é chamado como parte de uma operação de salvamento, o valor normalmente é **true**; quando chamado como parte de uma operação salvar como, o valor normalmente é **false**.)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método **IPersistStream:: Save** . Ele chama **WriteInt** com a versão do software, [**chama CPersistStream:: WriteToStream**](cpersiststream-writetostream.md) com o fluxo em *pStm* e redefine **mPS \_ fDirty**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




