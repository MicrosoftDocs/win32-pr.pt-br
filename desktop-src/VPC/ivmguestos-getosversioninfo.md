---
title: Método IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Recupera informações de versão para o sistema operacional convidado em execução na máquina virtual.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- GetOsVersionInfo do método virtual PC
- Método GetOsVersionInfo Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759168"
---
# <a name="ivmguestosgetosversioninfo-method"></a>Método IVMGuestOS:: GetOsVersionInfo

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera informações de versão para o sistema operacional convidado em execução na VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guestOsVersionInfo* \[ out, retval\]
</dt> <dd>

Um ponteiro para uma estrutura [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                       | Descrição                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | A operação foi bem-sucedida.<br/>                                  |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                               | O parâmetro é **NULL**.<br/>                                     |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl> | Não há memória suficiente disponível para concluir esta solicitação.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                       | Ocorreu um erro inesperado.<br/>                              |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>                  | A VM não está em execução.<br/>                                         |
| <dl> <dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt> </dl>    | Os componentes de integração não estão instalados nesta VM.<br/>           |



 

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

 

