---
title: Interface IVMKeyboard (VPCCOMInterfaces. h)
description: Controla o dispositivo de teclado em uma máquina virtual. O IVMKeyboard para uma máquina virtual pode ser recuperado usando a propriedade de teclado IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Virtual PC de interface IVMKeyboard
- Virtual PC de interface IVMKeyboard, descrito
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
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784983"
---
# <a name="ivmkeyboard-interface"></a>Interface IVMKeyboard

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla o dispositivo de teclado em uma máquina virtual. O **IVMKeyboard** para uma máquina virtual pode ser recuperado usando a propriedade [**IVMVirtualMachine:: Keyboard**](ivmvirtualmachine-keyboard.md) .

## <a name="members"></a>Membros

A interface **IVMKeyboard** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMKeyboard** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMKeyboard** tem esses métodos.



| Método                                                       | Descrição                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Ispressioned**](ivmkeyboard-ispressed.md)                   | Determina se a chave especificada está inativa.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simula uma tecla que está sendo pressionada e liberada.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simula uma tecla que está sendo pressionada.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simula uma chave que está sendo liberada.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simula uma série de chaves ASCII que estão sendo digitadas no convidado.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas no convidado.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMKeyboard** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso           | Descrição                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Leitura/gravação<br/> | Indica se este objeto tem controle exclusivo sobre o dispositivo de teclado da máquina virtual.<br/> |



 

## <a name="remarks"></a>Comentários

As chaves podem ser digitadas na máquina virtual de várias maneiras. Para digitar uma sequência ASCII normal de caracteres, use o método [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) . Se for necessária maior flexibilidade, o **IVMKeyboard** terá vários métodos projetados para serem usados com os códigos de chave na lista a seguir. O método [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) pode aceitar uma cadeia de caracteres delimitada por vírgulas de códigos de chave, que serão prensados e liberados, em ordem, dentro da máquina virtual. Além desses códigos-chave, as palavras-chave para cima e para baixo podem ser usadas para forçar uma tecla a ser pressionada apenas ou ser liberada. As palavras-chave para cima e para baixo aplicam-se apenas ao código de tecla diretamente após a palavra-chave.

Para evitar que vários scripts, aplicativos ou usuários tentem simultaneamente acessar o mesmo dispositivo de teclado, defina a propriedade [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) como **true**. Se o acesso exclusivo for adquirido por um processo, as tentativas feitas por outros processos para enviar a entrada para o dispositivo de teclado serão ignoradas até que o acesso exclusivo seja liberado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces do Windows Virtual PC](virtual-pc-interfaces.md)
</dt> <dt>

[Sequências de chave](key-sequences.md)
</dt> </dl>

 

