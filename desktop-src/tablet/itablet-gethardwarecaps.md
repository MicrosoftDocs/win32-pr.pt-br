---
description: Retorna um valor que representa os recursos do hardware do Tablet.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'Método ITablet:: GetHardwareCaps'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829691"
---
# <a name="itabletgethardwarecaps-method"></a>Método ITablet:: GetHardwareCaps

Retorna um valor que representa os recursos do hardware do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwCaps* \[ fora\]
</dt> <dd>

Sinalizadores de bits que representam os recursos do hardware do Tablet.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

O parâmetro *pdwCaps* é um conjunto de sinalizadores de bits que descrevem os recursos de hardware do Tablet. A tabela a seguir descreve esses sinalizadores.



| Nome do sinalizador                         | Valor                 | Descrição                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| THWC \_ integrado<br/>       | 0x00000001<br/> | Indica que a exibição e o digitalizador compartilham a mesma superfície.<br/>                                                    |
| o \_ CSR THWC \_ deve \_ tocar<br/> | 0x00000002<br/> | Indica que o cursor deve estar no contato físico com o dispositivo para a posição do relatório.<br/>                           |
| \_proximidade THWC \_<br/>  | 0x00000004<br/> | Indica que o dispositivo pode gerar eventos quando o cursor está entrando e saindo do intervalo de detecção física.<br/> |
| THWC \_ PHYSID \_ SACs<br/>     | 0x00000008<br/> | Indica que o dispositivo pode identificar exclusivamente o cursor ativo no hardware.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




