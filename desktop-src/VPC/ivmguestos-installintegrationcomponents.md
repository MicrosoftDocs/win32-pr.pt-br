---
title: Método IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces.h)
description: Localiza e instala os Componentes de Integração mais recentes no sistema operacional convidado.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Pc Virtual do método InstallIntegrationComponents
- Método InstallIntegrationComponents pc virtual, interface IVMGuestOS
- INTERFACE IVMGuestOS Pc Virtual , método InstallIntegrationComponents
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c61ade15736cec16976566f464573b30df7fd918f0f2be84f2f4ebd56e5db514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007186"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a>Método IVMGuestOS::InstallIntegrationComponents

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Localiza e instala os Componentes de Integração mais recentes no sistema operacional convidado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>                       | A máquina virtual deve estar em execução para essa operação.<br/>                     |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | Não foi possível encontrar a máquina virtual.<br/>                                     |
| <dl> <dt>**VM \_ E \_ UNIDADE \_ INVÁLIDA**</dt> <dt>0XA0040502</dt> </dl>                         | A máquina virtual não tem uma unidade de DVD vazia.<br/>                       |
| <dl> <dt>**VM \_ E \_ MEDIA \_ UNMOUNT \_ FALHA**</dt> <dt>0XA0040508</dt> </dl>                   | Falha na tentativa de desmontar a mídia da unidade de DVD da máquina virtual.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0X80070002</dt> </dl> | O sistema não pode encontrar o arquivo ISO para os Componentes de Integração.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

