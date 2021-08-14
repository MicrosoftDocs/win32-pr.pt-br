---
title: Interface IVMKeyboard (VPCCOMInterfaces.h)
description: Controla o dispositivo de teclado em uma máquina virtual. O IVMKeyboard para uma máquina virtual pode ser recuperado usando a propriedade IvMVirtualMachine Keyboard.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- COMPUTADOR Virtual da interface IVMKeyboard
- INTERFACE IVMKeyboard pc virtual , descrito
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7284c4e2bb164cd53c8a34357c881ed096f342ae2c2230422985fac4c1fdae9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344793"
---
# <a name="ivmkeyboard-interface"></a>Interface IVMKeyboard

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla o dispositivo de teclado em uma máquina virtual. O **IVMKeyboard** para uma máquina virtual pode ser recuperado usando a [**propriedade IVMVirtualMachine::Keyboard.**](ivmvirtualmachine-keyboard.md)

## <a name="members"></a>Membros

A **interface IVMKeyboard** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMKeyboard** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **interface IVMKeyboard** tem esses métodos.



| Método                                                       | Descrição                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Ispressed**](ivmkeyboard-ispressed.md)                   | Determina se a chave especificada está inobada.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simula uma tecla que está sendo pressionada e liberada.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simula uma tecla que está sendo pressionada.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simula uma chave que está sendo liberada.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simula uma série de chaves ASCII que estão sendo digitadas no convidado.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas no convidado.<br/> |



 

### <a name="properties"></a>Propriedades

A **interface IVMKeyboard** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso           | Descrição                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Leitura/gravação<br/> | Indica se esse objeto tem controle exclusivo sobre o dispositivo de teclado da máquina virtual.<br/> |



 

## <a name="remarks"></a>Comentários

As chaves podem ser digitadas na máquina virtual de várias maneiras. Para digitar uma sequência ASCII normal de caracteres, use o [**método TypeAsciiText.**](ivmkeyboard-typeasciitext.md) Se for necessária maior flexibilidade, **IVMKeyboard** terá vários métodos projetados para serem usados com os códigos-chave na lista a seguir. O [**método TypeKeySequence**](ivmkeyboard-typekeysequence.md) pode aceitar uma cadeia de caracteres delimitada por vírgulas de códigos de chave, que será pressionada e liberada, na ordem, dentro da máquina virtual. Além desses códigos-chave, as palavras-chave UP e DOWN podem ser usadas para forçar uma tecla a ser pressionada apenas ou ser liberadas apenas. As palavras-chave UP e DOWN se aplicam somente ao código-chave diretamente após a palavra-chave .

Para evitar vários scripts, aplicativos ou usuários de tentarem acessar simultaneamente o mesmo dispositivo de teclado, de definir a propriedade [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) como **TRUE.** Se o acesso exclusivo for adquirido por um processo, todas as tentativas de outros processos de enviar entrada para o dispositivo de teclado serão ignoradas até que o acesso exclusivo seja liberado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Virtual PC Interfaces](virtual-pc-interfaces.md)
</dt> <dt>

[Sequências de chaves](key-sequences.md)
</dt> </dl>

 

