---
title: Método IEnumProgressItems RemoteNext
description: Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração. | Método IEnumProgressItems RemoteNext
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Método RemoteNext IMAPi
- Método RemoteNext IMAPi, interface IEnumProgressItems
- IEnumProgressItems interface IMAPi, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daa2b33fdc356782837aadfe37186bc4cc2b493208fdc78ba645ada9e746582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884846"
---
# <a name="ienumprogressitemsremotenext-method"></a>Método IEnumProgressItems:: RemoteNext

Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Número de itens a serem recuperados.

</dd> <dt>

*rgelt* \[ fora\]
</dt> <dd>

Matriz de interfaces [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) . Você deve liberar cada interface em rgelt quando terminar.

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Número de elementos retornados em rgelt. Você pode definir *pceltFetched* como **NULL** se *celt* for um. Caso contrário, inicialize o valor de *pceltFetched* como 0 antes de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

S \_ OK é retornado quando o número de elementos solicitados (*celt*) é retornado com êxito ou o número de itens retornados (*pceltFetched*) é menor que o número de elementos solicitados.

Outros códigos de êxito podem ser retornados como resultado da implementação. Os códigos de erro a seguir são normalmente retornados na falha da operação, mas não representam os únicos valores de erro possíveis:



| Código de retorno                                                                                   | Descrição                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O ponteiro não é válido.<br/> Valor: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Falha ao alocar a memória necessária.<br/> Valor: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um ou mais argumentos não são válidos.<br/> Valor: 0x80070057<br/>    |
| <dl> <dt>**E \_ Inesperado**</dt> </dl> | Ocorreu uma falha inesperada.<br/> Valor: 0x8000FFFF<br/>         |



 

## <a name="remarks"></a>Comentários

Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, somente Windows XP com \[ aplicativos de área de trabalho do SP2\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| INSERI<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumProgressItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[IEnumProgressItems:: Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





