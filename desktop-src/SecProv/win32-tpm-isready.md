---
description: Indica se o TPM está pronto para uso.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: 'Método Win32_Tpm:: IsReady'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8a04f2e834a77582698ff8f16e7a680db53474fa8c214556eb168c477afe58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004064"
---
# <a name="win32_tpmisready-method"></a>\_Método TPM:: IsReady do Win32

Indica se o TPM está pronto para uso.

Esse método só pode ser acessado por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsReady* \[ fora\]
</dt> <dd>

Defina como **true** se o TPM e o sistema forem totalmente provisionados para uso do TPM.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
