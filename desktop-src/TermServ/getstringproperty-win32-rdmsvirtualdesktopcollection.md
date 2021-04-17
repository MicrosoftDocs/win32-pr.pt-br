---
title: Método getstringproperty da classe Win32_RDMSVirtualDesktopCollection
description: Recupera uma propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753524"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método getstringproperty da classe Win32 \_ RDMSVirtualDesktopCollection

Recupera uma propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

Uma chave que identifica a propriedade a ser recuperada.

</dd> <dt>

*Valor* \[ do fora\]
</dt> <dd>

Uma cadeia de caracteres que recebe o valor recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





