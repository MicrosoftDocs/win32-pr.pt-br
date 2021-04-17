---
title: Enumeração TYPEmode (Softkbdc. h)
description: Elementos da enumeração TYPEmode são usados para especificar modos de tipo que estão disponíveis para um teclado virtual.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Estrutura de serviços de texto de enumeração do TIPOmode
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757230"
---
# <a name="typemode-enumeration"></a>Enumeração TYPEmode

Elementos da enumeração **typemode** são usados para especificar modos de tipo que estão disponíveis para um teclado virtual.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**
</dt> <dd>

O usuário pode clicar nas chaves na tela para digitar o texto.

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Operação**
</dt> <dd>

O usuário pode apontar para uma chave por um período de tempo predefinido e o caractere selecionado é digitado automaticamente.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Varredura**
</dt> <dd>

O teclado virtual verifica continuamente a área de entrada e realça as regiões em que o usuário pode pressionar uma tecla de atalho ou usar um dispositivo de entrada de interruptor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





