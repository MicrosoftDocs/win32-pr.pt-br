---
title: Método getint32property da classe Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera uma propriedade de número inteiro de uma coleção de áreas de trabalho virtuais.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- Método getint32property Serviços de Área de Trabalho Remota
- Método getint32property Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método getint32property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764745"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método getint32property da classe Win32 \_ RDMSVirtualDesktopCollection

Recupera uma propriedade de número inteiro de uma coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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

Um inteiro que recebe o valor recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                                   |
| parâmetro<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





