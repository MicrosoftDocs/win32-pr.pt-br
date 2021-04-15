---
title: Método IEnumFsiItems RemoteNext
description: Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração. | Método IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Método RemoteNext IMAPi
- Método RemoteNext IMAPi, interface IEnumFsiItems
- IEnumFsiItems interface IMAPi, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506414"
---
# <a name="ienumfsiitemsremotenext-method"></a>Método IEnumFsiItems:: RemoteNext

Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
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

Matriz de interfaces [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) . Você deve liberar cada interface em rgelt quando terminar.

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Número de elementos retornados em rgelt. Você pode definir *pceltFetched* como **NULL** se *celt* for um. Caso contrário, inicialize o valor de *pceltFetched* como 0 antes de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

S \_ OK é retornado quando o número de elementos solicitados (*celt*) é retornado com êxito ou o número de itens retornados (*pceltFetched*) é menor que o número de elementos solicitados.

Outros códigos de êxito podem ser retornados como resultado da implementação. Os códigos de erro a seguir são normalmente retornados na falha da operação, mas não representam os únicos valores de erro possíveis:



| Código de retorno                                                                                   | Descrição                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O ponteiro não é válido.<br/> Valor: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Falha ao alocar a memória necessária.<br/> Valor: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um ou mais argumentos não são válidos.<br/> Valor: 0x80070057<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP2\]<br/>                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| INSERI<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumFsiItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[IEnumFsiItems:: Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





