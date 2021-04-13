---
title: Método getParameter IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera um parâmetro nomeado dentro do sistema operacional convidado.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- PC virtual do método getParameter
- Método getParameter Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método getParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499714"
---
# <a name="ivmguestosgetparameter-method"></a>Método IVMGuestOS:: getParameter

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um parâmetro nomeado dentro do sistema operacional convidado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Inparametrizaname* \[ no\]
</dt> <dd>

O nome do parâmetro. Ele deve ter entre 1 e 255 caracteres de comprimento e não pode conter uma barra invertida ( \) caractere.

</dd> <dt>

*ParameterValue* \[ out, retval\]
</dt> <dd>

O valor do parâmetro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                    | Descrição                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Um parâmetro não é válido ou não foi especificado.<br/>                        |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro é **NULL**.<br/>                                        |
| <dl> <dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt> </dl>                     | A operação não foi concluída oportunamente.<br/>                |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual não está em execução.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM em \_ pausa**</dt> <dt>0xA00400507</dt> </dl>                    | A máquina virtual está pausada.<br/>                                    |
| <dl> <dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt> </dl> | Os componentes de integração não estão instalados nesta máquina virtual.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                 |



 

## <a name="remarks"></a>Comentários

A máquina virtual deve estar em execução e os componentes de integração devem ser instalados quando esse método é invocado. Esse método só tem suporte em sistemas operacionais convidados baseados no Windows.

Com os componentes de integração instalados, a chave a seguir é automaticamente adicionada ao registro do sistema operacional convidado:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Quando o sistema operacional convidado é iniciado, os seguintes valores de cadeia de caracteres do registro são populados na chave de **parâmetros** :

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

