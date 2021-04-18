---
description: Obtém um novo fluxo para o item especificado.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Método IWiaTransferCallback:: GetNextStream (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764019"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a>Método IWiaTransferCallback:: GetNextStream

Obtém um novo fluxo para o item especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*bstrItemName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do item para o qual criar o fluxo.

</dd> <dt>

*bstrFullItemName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome completo do item para o qual criar o fluxo.

</dd> <dt>

*ppDestination* \[ fora\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***

Recebe o endereço de um ponteiro para o novo objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Quando esse método é implementado por um filtro de processamento de imagem, a minidriver de aquisição de imagens do Windows (WIA) 2,0 o chama durante a aquisição da imagem para obter o fluxo de destino do cliente.

**IWiaTransferCallback:: GetNextStream** de um filtro deve delegar ao método de retorno de chamada do aplicativo. O filtro usa o fluxo retornado pela implementação **IWiaTransferCallback:: GetNextStream** do retorno de chamada do aplicativo para criar seu próprio fluxo que passa de volta para o serviço WIA 2,0. A filtragem é feita quando o fluxo do filtro chama o método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .

O fluxo do filtro não pode fazer suposições sobre o número de bytes gravados nele em cada gravação, já que os dados da imagem não filtrada podem vir do componente de visualização do WIA 2,0 em vez do driver. O componente de visualização do WIA 2,0 sempre grava todos os dados de imagem não filtrados no fluxo do filtro apenas uma vez, o que significa que o fluxo do filtro tem uma fonte que está gravando. Se o driver e o componente de visualização gravarem no fluxo do filtro, o fluxo do filtro não poderá supor, por exemplo, que ele receberá o cabeçalho completo na primeira vez que [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) for chamado, embora seu driver correspondente sempre grave os dados de cabeçalho primeiro em uma gravação. Nem é possível pressupor que uma gravação subsequente contém exatamente uma linha de verificação. Portanto, o fluxo de filtragem pode ter que contar o número de bytes gravados para determinar, por exemplo, onde os dados da imagem são iniciados.

A implementação de **IWiaTransferCallback:: GetNextStream** do filtro de processamento de imagens deve ler as propriedades necessárias para seu processamento de imagem do item para o qual a imagem está sendo adquirida. O filtro não lê as propriedades diretamente do *pWiaItem2* passado para [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md). Em vez disso, o filtro deve chamar [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) neste item WIA 2,0 para obter o item atual do WIA 2,0. O motivo disso é que a imagem que está sendo adquirida pode ser, na verdade, um item filho de *pWiaItem2*. Por exemplo, durante uma aquisição de pasta, o filtro usa *pWiaItem2* para obter itens filho de *pWiaItem2* em **IWiaTransferCallback:: GetNextStream** (durante uma aquisição de pasta, o driver retorna as imagens representadas pelos itens filho de *pWiaItem2*). O mesmo acontece quando o componente de visualização do WIA 2,0 chama o filtro de processamento de imagem, passando um item filho WIA 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
