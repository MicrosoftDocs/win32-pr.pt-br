---
description: O novo método inicializa um comando a ser executado e retorna um novo objeto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Método CCmdQueue. New (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757706"
---
# <a name="ccmdqueuenew-method"></a>Método CCmdQueue. New

O `New` método inicializa um comando a ser executado e retorna um novo objeto [**CDeferredCommand**](cdeferredcommand.md) .

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppCmd* 
</dt> <dd>

Endereço de um ponteiro para um objeto [**CDeferredCommand**](cdeferredcommand.md) pelo qual um aplicativo pode cancelar o comando, definir um novo horário de apresentação para ele ou recuperar informações de estimativa.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o objeto que executará o comando.

</dd> <dt>

*time* 
</dt> <dd>

Hora em que o comando ou comandos enfileirados são executados.

</dd> <dt>

*IID* 
</dt> <dd>

Ponteiro para o identificador global exclusivo (**GUID**) da interface a ser chamada.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método na interface a ser chamada.

</dd> <dt>

*wFlags* 
</dt> <dd>

Sinalizadores que descrevem o contexto da chamada. Esse parâmetro oferece suporte aos mesmos sinalizadores que o método **IDispatch:: Invoke** .

</dd> <dt>

*cArgs* 
</dt> <dd>

Número de argumentos passados.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Ponteiro para a lista de tipos variantes associados aos parâmetros de expedição.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Ponteiro para a lista em que os resultados, se houver, devem ser retornados.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Ponteiro para o índice na lista de parâmetros *pDispParams* em que ocorreu o último erro.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica se o parâmetro de *tempo* é um valor de tempo de transmissão (**true**) ou um valor de tempo de apresentação (**false**).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Retorna E \_ OUTOFMEMORY se *ppCmd* retornar da criação do novo objeto [**CDeferredCommand**](cdeferredcommand.md) com um valor de **NULL**. Caso contrário, retorna um **HRESULT** que indica um erro ao tentar criar um novo objeto **CDeferredCommand** . Se houver um erro, nenhum objeto será colocado na fila.

## <a name="remarks"></a>Comentários

O novo objeto [**CDeferredCommand**](cdeferredcommand.md) será inicializado com os parâmetros e será adicionado à fila durante a construção. Esse método é semelhante ao método **IDispatch:: Invoke** .

Os valores para o parâmetro *wFlags* incluem o seguinte:



| Valor                    | Descrição                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| método de expedição \_         | O membro está sendo executado como um método. Se uma propriedade tiver o mesmo nome, isso e o \_ sinalizador PROPERTYGET de expedição poderão ser definidos.                                       |
| PROPERTYGET de expedição \_    | O membro está sendo recuperado como uma propriedade ou um membro de dados.                                                                                                          |
| PROPERTYPUT de expedição \_    | O membro está sendo alterado como um membro de propriedade ou de dados.                                                                                                            |
| PROPERTYPUTREF de expedição \_ | O membro está sendo alterado por meio de uma atribuição de referência, em vez de uma atribuição de valor. Esse valor é válido somente quando a propriedade aceita uma referência a um objeto. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




