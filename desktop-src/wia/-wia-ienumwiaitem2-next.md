---
description: Preenche uma matriz de ponteiros para interfaces IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'Método IEnumWiaItem2:: Next (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164712"
---
# <a name="ienumwiaitem2next-method"></a>Método IEnumWiaItem2:: Next

Preenche uma matriz de ponteiros para interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cElt* \[ no\]
</dt> <dd>

Tipo: **ULONG**

Especifica o número de elementos de matriz na matriz indicado pelo parâmetro *ppIWiaItem2* .

</dd> <dt>

*ppIWiaItem2* \[ fora\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de uma matriz de ponteiros de interface [**IWiaItem2**](-wia-iwiaitem2.md) . **IEnumWiaItem2:: Next** preenche essa matriz com ponteiros de interface.

</dd> <dt>

*pcEltFetched* \[ entrada, saída\]
</dt> <dd>

Tipo: **ULONG \** _

Na saída, esse parâmetro recebe o número de ponteiros de interface realmente armazenados na matriz indicada pelo parâmetro _ppIWiaItem2 *. Quando a enumeração for concluída, esse parâmetro conterá zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O sistema de tempo de execução do WIA (Windows Image Acquisition) 2,0 representa os dispositivos de hardware WIA 2,0 como uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) . Os aplicativos usam o método **IEnumWiaItem2:: Next** para obter um ponteiro de interface **IWiaItem2** para cada item na pasta atual da árvore de objetos **IWiaItem2** de um dispositivo de hardware.

Para obter a lista de ponteiros, o aplicativo passa uma matriz de ponteiros de interface [**IWiaItem2**](-wia-iwiaitem2.md) que ele aloca. Ele também passa o número de elementos de matriz no parâmetro *cElt*. O método **IEnumWiaItem2:: Next** preenche a matriz com ponteiros para interfaces **IWiaItem2** .

Até que o processo de enumeração seja concluído, o método **IEnumWiaItem2:: Next** retorna S \_ OK. A cada vez, ele define o valor apontado por *pcEltFetched* para o número de itens inseridos na matriz. Quando **IEnumWiaItem2:: Next** termina o processo de enumeração de objetos [**IWiaItem2**](-wia-iwiaitem2.md) , ele retorna S \_ false e define o local da memória apontado por *pcEltFetched* como zero.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIWiaItem2* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
