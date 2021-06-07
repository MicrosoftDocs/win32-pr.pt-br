---
title: Método IVMGuestOS SetParameter (VPCCOMInterfaces.h)
description: Define um parâmetro nomeado dentro do sistema operacional convidado.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Computador Virtual do método SetParameter
- Método SetParameter Pc Virtual, interface IVMGuestOS
- INTERFACE IVMGuestOS pc virtual, método SetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc99d9b38ab43327b4a435c4128378d49682935
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386705"
---
# <a name="ivmguestossetparameter-method"></a>Método IVMGuestOS::SetParameter

\[O Computador Virtual do Windows não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define um parâmetro nomeado dentro do sistema operacional convidado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inParameterName* \[ Em\]
</dt> <dd>

O nome do parâmetro. Ele deve ter entre 1 e 255 caracteres e não pode conter um caractere de invertida ( \\ ).

</dd> <dt>

*inParameterValue* \[ Em\]
</dt> <dd>

O valor do parâmetro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                    | Descrição                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Um parâmetro não é válido ou não especificado.<br/>           |
| <dl> <dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt> </dl>                     | A operação não foi concluída em tempo hábil.<br/>   |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>               | A VM (máquina virtual) não está em execução.<br/>             |
| <dl> <dt>**VM \_ E \_ VM \_ PAUSADA**</dt> <dt>0xA00400507</dt> </dl>                    | A VM está em pausa.<br/>                                    |
| <dl> <dt>**VM \_ O \_ RECURSO DE \_ ADIÇÕES E NÃO \_ \_ É**</dt> <dt>0XA0040505</dt> </dl> | Os componentes de integração não estão instalados nessa VM.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                    |



 

## <a name="remarks"></a>Comentários

A VM deve estar em execução e os componentes de integração devem ser instalados quando esse método é invocado. Esse método só tem suporte para sistemas operacionais convidados baseados no Windows.

Com os componentes de integração instalados, a seguinte chave é adicionada automaticamente ao registro do sistema operacional convidado:

**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Quando o sistema operacional convidado é iniciado, os seguintes valores de cadeia de caracteres do Registro são preenchidos na **chave Parâmetros:**

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos \[ da área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

