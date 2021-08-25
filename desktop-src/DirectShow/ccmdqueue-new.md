---
description: O novo método inicializa um comando a ser executado e retorna um novo objeto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Método CCmdQueue.New (Winutil.h)
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
ms.openlocfilehash: c8b6ad22b67df863e699649f22f513a98ca1306751a1d449a683f306c9cc2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910386"
---
# <a name="ccmdqueuenew-method"></a>Método CCmdQueue.New

O `New` método inicializa um comando a ser executado e retorna um novo objeto [**CDeferredCommand.**](cdeferredcommand.md)

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

Endereço de um ponteiro para um [**objeto CDeferredCommand**](cdeferredcommand.md) pelo qual um aplicativo pode cancelar o comando, definir um novo tempo de apresentação para ele ou recuperar informações de estimativa.

</dd> <dt>

*Punk* 
</dt> <dd>

Ponteiro para o objeto que executará o comando.

</dd> <dt>

*time* 
</dt> <dd>

Hora em que executar o comando ou comandos na fila.

</dd> <dt>

*Iid* 
</dt> <dd>

Ponteiro para o **GUID**(identificador global exclusivo) da interface a ser chamada.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Método na interface a ser chamado.

</dd> <dt>

*Wflags* 
</dt> <dd>

Sinalizadores que descrevem o contexto da chamada. Esse parâmetro dá suporte aos mesmos sinalizadores que **o método IDispatch::Invoke.**

</dd> <dt>

*Cargs* 
</dt> <dd>

Número de argumentos passados.

</dd> <dt>

*Pdispparams* 
</dt> <dd>

Ponteiro para a lista de tipos variantes associados aos parâmetros de expedição.

</dd> <dt>

*Pvarresult* 
</dt> <dd>

Ponteiro para a lista em que os resultados, se algum, devem ser retornados.

</dd> <dt>

*Puargerr* 
</dt> <dd>

Ponteiro para o índice dentro da *lista de parâmetros pDispParams* em que ocorreu o último erro.

</dd> <dt>

*bStream* 
</dt> <dd>

Valor que indica se o *parâmetro time* é um valor de tempo de fluxo (**TRUE**) ou um valor de tempo de apresentação (**FALSE**).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido. Retornará E \_ OUTOFMEMORY se *ppCmd* retornar da criação do novo objeto [**CDeferredCommand**](cdeferredcommand.md) com um valor **null**. Caso contrário, retornará **um HRESULT** que indica um erro ao tentar criar um novo **objeto CDeferredCommand.** Se houver um erro, nenhum objeto foi en fila.

## <a name="remarks"></a>Comentários

O novo [**objeto CDeferredCommand**](cdeferredcommand.md) será inicializado com os parâmetros e será adicionado à fila durante a construção. Esse método é semelhante ao **método IDispatch::Invoke.**

Os valores para *o parâmetro wFlags* incluem o seguinte:



| Valor                    | Descrição                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MÉTODO \_ DISPATCH         | O membro está sendo executado como um método. Se uma propriedade tiver o mesmo nome, este e o sinalizador DISPATCH \_ PROPERTYGET poderão ser definidos.                                       |
| DISPATCH \_ PROPERTYGET    | O membro está sendo recuperado como uma propriedade ou membro de dados.                                                                                                          |
| DISPATCH \_ PROPERTYPUT    | O membro está sendo alterado como uma propriedade ou membro de dados.                                                                                                            |
| DISPATCH \_ PROPERTYPUTREF | O membro está sendo alterado por meio de uma atribuição de referência, em vez de uma atribuição de valor. Esse valor é válido somente quando a propriedade aceita uma referência a um objeto . |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




