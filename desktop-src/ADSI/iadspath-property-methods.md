---
title: Métodos de propriedade IADsPath (IADs. h)
description: O método Property da interface IADsPath define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPath
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644945"
---
# <a name="iadspath-property-methods"></a>Métodos de propriedade IADsPath

O método Property da interface [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Caminho**
</dt> <dd> <dl>

Caminho de um diretório do sistema de arquivos.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**Tipo**
</dt> <dd> <dl>

Tipo de arquivo do sistema de arquivos.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

**VolumeName**
</dt> <dd> <dl>

Nome de um volume existente do sistema de arquivos.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPath é definido como B287FCD5-4080-11D1-A3AC-00C04FB950DC<br/>             |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[**\_caminho ADs**](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





