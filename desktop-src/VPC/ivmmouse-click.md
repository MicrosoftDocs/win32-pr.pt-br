---
title: Método IVMMouse Click (VPCCOMInterfaces.h)
description: Simula um clique de botão do mouse.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Clique no método Virtual PC
- Clique no método Virtual PC , interface IVMMouse
- INTERFACE IVMMouse pc virtual , método Click
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d1d1aaf538ac6b30a27df904729f2ad3187ebde29cb915c3d7ef35d1e9cf57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974237"
---
# <a name="ivmmouseclick-method"></a>Método IVMMouse::Click

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula um clique de botão do mouse.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*buttonIndex* \[ Em\]
</dt> <dd>

O índice do botão que está sendo clicado. Para ver uma lista de valores, [**consulte VMMouseButton**](vmmousebutton.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                        | Descrição                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | A operação foi bem-sucedida.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | O parâmetro é **NULL.**<br/>                                                                                                             |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>   | A máquina virtual à qual este dispositivo do mouse está anexado não está em execução no momento.<br/>                                                   |
| <dl> <dt>**VM \_ E \_ MOUSE NÃO ATIVO \_ \_ 0XA0040800**</dt> <dt></dt> </dl> | A operação não pôde ser concluída porque o dispositivo do mouse não está ligado ou não está ativo na máquina virtual no momento.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>        | Ocorreu um erro inesperado.<br/>                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse é definido como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

